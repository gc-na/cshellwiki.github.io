# [Linux] Bash hexdump 用法: 显示文件的十六进制转储

## 概述
`hexdump` 命令用于以十六进制格式显示文件的内容，常用于调试和分析二进制文件。它可以帮助用户查看文件的原始数据，便于理解文件的结构和内容。

## 用法
基本语法如下：
```
hexdump [options] [arguments]
```

## 常用选项
- `-C`：以传统的十六进制格式和 ASCII 字符同时显示。
- `-n <数目>`：仅显示指定字节数的内容。
- `-v`：显示所有数据，不压缩重复的行。
- `-e <格式>`：自定义输出格式。

## 常见示例
1. 显示文件的十六进制内容：
   ```bash
   hexdump filename.txt
   ```

2. 以传统格式和 ASCII 字符同时显示：
   ```bash
   hexdump -C filename.bin
   ```

3. 仅显示文件的前 16 个字节：
   ```bash
   hexdump -n 16 filename.txt
   ```

4. 自定义输出格式：
   ```bash
   hexdump -e '16/1 "%02x " "\n"' filename.txt
   ```

5. 显示所有数据，包括重复行：
   ```bash
   hexdump -v filename.bin
   ```

## 提示
- 在处理大文件时，使用 `-n` 选项可以避免输出过多数据。
- 使用 `-C` 选项可以更容易地理解二进制数据，因为它同时显示十六进制和 ASCII。
- 如果需要分析特定的字节序列，可以结合使用 `grep` 命令来过滤输出。