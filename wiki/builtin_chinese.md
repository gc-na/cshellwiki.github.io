# [Linux] Bash builtin 内置命令: 显示当前 shell 的内置命令

## 概述
内置命令 `builtin` 用于执行 Bash 内置命令，而不调用外部命令。这在需要确保使用内置版本的命令时非常有用。

## 用法
基本语法如下：
```bash
builtin [options] [arguments]
```

## 常用选项
- `-f` : 忽略函数定义，直接调用内置命令。
- `-p` : 使用路径查找内置命令。

## 常见示例
1. 调用内置的 `echo` 命令：
   ```bash
   builtin echo "Hello, World!"
   ```

2. 忽略函数定义，直接调用内置的 `cd` 命令：
   ```bash
   builtin -f cd /path/to/directory
   ```

3. 使用路径查找内置的 `type` 命令：
   ```bash
   builtin -p type echo
   ```

## 提示
- 在脚本中使用 `builtin` 可以确保你调用的是内置命令而不是同名的外部命令。
- 如果你重定义了某个内置命令，使用 `builtin` 可以恢复到原始的内置功能。
- 在调试脚本时，使用 `builtin` 可以帮助你确认命令的来源。