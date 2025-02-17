# [Linux] Bash sha256sum 用法: 计算文件的SHA-256哈希值

## 概述
`sha256sum` 命令用于计算并输出文件的SHA-256哈希值。SHA-256是一种加密哈希函数，广泛用于数据完整性验证和安全性检查。

## 用法
基本语法如下：
```bash
sha256sum [options] [arguments]
```

## 常用选项
- `-b`：以二进制模式读取文件。
- `-c`：检查给定的SHA-256哈希值是否与文件匹配。
- `--help`：显示帮助信息。
- `--version`：显示版本信息。

## 常见示例
1. 计算文件的SHA-256哈希值：
   ```bash
   sha256sum example.txt
   ```

2. 将哈希值输出到文件：
   ```bash
   sha256sum example.txt > example.txt.sha256
   ```

3. 验证文件的哈希值：
   ```bash
   sha256sum -c example.txt.sha256
   ```

4. 计算多个文件的哈希值：
   ```bash
   sha256sum file1.txt file2.txt
   ```

## 提示
- 在验证文件时，确保哈希值文件与待验证文件在同一目录下。
- 使用 `-b` 选项可以确保正确处理二进制文件。
- 定期检查文件的哈希值，以确保数据的完整性和安全性。