# [Linux] Bash split 用法: 将文件拆分成多个小文件

## 概述
`split` 命令用于将一个大文件拆分成多个较小的文件，便于处理和传输。它可以根据行数或字节数来拆分文件，适用于处理大数据文件时的需求。

## 用法
基本语法如下：
```bash
split [选项] [参数]
```

## 常用选项
- `-l NUM`：按行数拆分文件，NUM 是每个输出文件的行数。
- `-b SIZE`：按字节数拆分文件，SIZE 是每个输出文件的字节数。
- `-d`：使用数字后缀而不是字母后缀。
- `--additional-suffix=SUFFIX`：为输出文件添加额外的后缀。

## 常见示例
1. 按行数拆分文件：
   ```bash
   split -l 1000 largefile.txt
   ```
   这将把 `largefile.txt` 拆分成每个包含 1000 行的小文件。

2. 按字节数拆分文件：
   ```bash
   split -b 1M largefile.txt
   ```
   这将把 `largefile.txt` 拆分成每个大小为 1MB 的小文件。

3. 使用数字后缀：
   ```bash
   split -d -l 500 largefile.txt part_
   ```
   这将把 `largefile.txt` 拆分成每个包含 500 行的小文件，并使用数字后缀（如 part_00, part_01）。

4. 添加额外后缀：
   ```bash
   split -l 200 largefile.txt --additional-suffix=.txt part_
   ```
   这将把文件拆分并为每个输出文件添加 `.txt` 后缀。

## 提示
- 在拆分大文件时，选择合适的行数或字节数可以提高处理效率。
- 使用 `-d` 选项可以避免文件名冲突，特别是在多次拆分时。
- 拆分后的文件可以使用 `cat` 命令轻松合并，确保数据完整性。