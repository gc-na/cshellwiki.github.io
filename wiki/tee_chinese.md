# [Linux] Bash tee 用法： 将输出写入文件和标准输出

## 概述
`tee` 命令用于将标准输入的数据同时输出到标准输出和一个或多个文件中。这使得用户可以在查看输出的同时，将其保存到文件中。

## 用法
基本语法如下：
```bash
tee [选项] [文件...]
```

## 常用选项
- `-a`：以追加模式写入文件，而不是覆盖。
- `-i`：忽略中断信号。
- `-p`：在写入文件之前，先打印到标准输出。

## 常见示例
1. 将输出写入文件：
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. 将输出追加到文件：
   ```bash
   echo "Another line" | tee -a output.txt
   ```

3. 同时写入多个文件：
   ```bash
   echo "Logging data" | tee file1.txt file2.txt
   ```

4. 使用 `-i` 选项忽略中断：
   ```bash
   cat somefile.txt | tee -i output.txt
   ```

## 提示
- 使用 `-a` 选项可以避免覆盖文件内容，适用于日志记录。
- 可以结合其他命令使用 `tee`，例如在管道中使用，以便在处理数据的同时保存输出。
- 注意文件权限，确保有权限写入指定的文件。