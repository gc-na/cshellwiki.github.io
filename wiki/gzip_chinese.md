# [Linux] Bash gzip 用法: 文件压缩工具

## 概述
`gzip` 是一个用于文件压缩的命令行工具，主要用于减少文件的大小，以便节省存储空间或加快传输速度。它使用 DEFLATE 算法进行压缩，通常用于压缩文本文件。

## 用法
基本语法如下：
```
gzip [选项] [参数]
```

## 常用选项
- `-d`：解压缩文件。
- `-k`：保留原始文件，压缩后仍然保留未压缩的文件。
- `-v`：显示详细的压缩过程信息。
- `-f`：强制压缩，即使文件已经存在。
- `-r`：递归地压缩目录中的所有文件。

## 常见示例
1. 压缩文件：
   ```bash
   gzip example.txt
   ```
   这将创建一个名为 `example.txt.gz` 的压缩文件，并删除原始的 `example.txt` 文件。

2. 解压缩文件：
   ```bash
   gzip -d example.txt.gz
   ```
   这将解压缩 `example.txt.gz` 文件，恢复为 `example.txt`。

3. 保留原始文件：
   ```bash
   gzip -k example.txt
   ```
   这将压缩 `example.txt`，并保留原始文件。

4. 递归压缩目录：
   ```bash
   gzip -r my_directory/
   ```
   这将递归压缩 `my_directory` 目录中的所有文件。

5. 显示详细信息：
   ```bash
   gzip -v example.txt
   ```
   这将显示压缩过程中的详细信息。

## 小贴士
- 在压缩大文件时，可以使用 `-f` 选项来覆盖已存在的压缩文件。
- 使用 `-k` 选项可以避免丢失原始文件，特别是在测试压缩效果时。
- 结合 `tar` 命令使用，可以更方便地压缩整个目录，例如：
   ```bash
   tar -czf archive.tar.gz my_directory/
   ```
   这将创建一个名为 `archive.tar.gz` 的压缩档案，包含 `my_directory` 目录及其内容。