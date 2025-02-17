# [Linux] Bash md5sum 用法: 计算文件的MD5哈希值

## 概述
`md5sum` 命令用于计算和验证文件的MD5哈希值。MD5哈希值是一个128位的散列值，通常用于检查文件的完整性。

## 用法
基本语法如下：
```
md5sum [选项] [参数]
```

## 常用选项
- `-b`：以二进制模式读取文件。
- `-c`：检查给定的MD5校验和文件。
- `-t`：以文本模式读取文件。
- `--help`：显示帮助信息。

## 常见示例
1. 计算单个文件的MD5哈希值：
   ```bash
   md5sum filename.txt
   ```

2. 计算多个文件的MD5哈希值：
   ```bash
   md5sum file1.txt file2.txt file3.txt
   ```

3. 将文件的MD5哈希值输出到文件中：
   ```bash
   md5sum filename.txt > checksum.md5
   ```

4. 检查MD5校验和：
   ```bash
   md5sum -c checksum.md5
   ```

## 提示
- 在处理大文件时，使用 `-b` 选项可以提高计算效率。
- 定期检查文件的MD5哈希值可以帮助确保数据的完整性。
- 在共享文件时，提供MD5哈希值可以让接收者验证文件是否未被篡改。