# [Linux] Bash cp 使用方法: 复制文件和目录

## 概述
`cp` 命令用于在 Linux 和 Unix 系统中复制文件和目录。它可以将一个或多个源文件复制到目标位置。

## 用法
基本语法如下：
```
cp [选项] [参数]
```

## 常用选项
- `-r`：递归复制目录及其内容。
- `-i`：在覆盖文件之前提示用户确认。
- `-u`：仅在源文件比目标文件新时才进行复制。
- `-v`：在复制过程中显示详细信息。

## 常见示例
1. 复制单个文件：
   ```bash
   cp file1.txt file2.txt
   ```
   这将把 `file1.txt` 复制为 `file2.txt`。

2. 复制多个文件到目录：
   ```bash
   cp file1.txt file2.txt /path/to/directory/
   ```
   这将把 `file1.txt` 和 `file2.txt` 复制到指定目录。

3. 递归复制目录：
   ```bash
   cp -r /source/directory /destination/directory
   ```
   这将把整个目录及其内容复制到目标位置。

4. 使用交互模式复制文件：
   ```bash
   cp -i file1.txt file2.txt
   ```
   如果 `file2.txt` 已存在，系统会提示确认是否覆盖。

5. 仅在源文件更新时复制：
   ```bash
   cp -u file1.txt file2.txt
   ```
   这将只在 `file1.txt` 比 `file2.txt` 新时进行复制。

## 提示
- 在复制重要文件时，使用 `-i` 选项可以避免意外覆盖。
- 使用 `-v` 选项可以帮助你跟踪复制进程，特别是在复制大量文件时。
- 确保目标路径存在，尤其是在复制目录时，避免出现错误。