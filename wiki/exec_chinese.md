# [Linux] Bash exec 用法: 执行命令并替换当前进程

## 概述
`exec` 命令用于在当前 shell 中执行指定的命令，并用该命令替换当前的 shell 进程。这意味着一旦执行了 `exec`，当前的 shell 将不再存在，取而代之的是新执行的命令。

## 用法
基本语法如下：
```bash
exec [选项] [命令] [参数]
```

## 常用选项
- `-a`：指定替代程序的名称。
- `-l`：将当前 shell 变为登录 shell。
- `-p`：使用父进程的环境变量。

## 常见示例
1. 替换当前 shell 进程为 `bash`：
   ```bash
   exec bash
   ```

2. 使用 `exec` 执行一个脚本并替换当前进程：
   ```bash
   exec ./myscript.sh
   ```

3. 以新的环境变量执行命令：
   ```bash
   exec -a myname /usr/bin/env
   ```

4. 使用 `exec` 启动一个登录 shell：
   ```bash
   exec -l bash
   ```

## 提示
- 使用 `exec` 时要小心，因为它会替换当前 shell 进程，无法返回到原来的 shell。
- 在脚本中使用 `exec` 可以提高性能，因为它不需要创建新的进程。
- 可以通过 `exec > output.txt` 将标准输出重定向到文件，从而将后续命令的输出写入该文件。