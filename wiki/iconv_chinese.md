# [Linux] Bash iconv 使用指南: 转换文件编码

## 概述
`iconv` 命令用于转换文件的字符编码。它可以将文本文件从一种编码格式转换为另一种编码格式，广泛应用于处理不同语言和字符集的文本数据。

## 用法
基本语法如下：
```bash
iconv [options] [arguments]
```

## 常用选项
- `-f`：指定源文件的编码格式。
- `-t`：指定目标文件的编码格式。
- `-o`：指定输出文件名。
- `-c`：忽略无法转换的字符。

## 常见示例
1. 将 UTF-8 编码的文件转换为 ISO-8859-1 编码：
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. 将 GBK 编码的文件转换为 UTF-8 编码：
   ```bash
   iconv -f GBK -t UTF-8 input.txt -o output.txt
   ```

3. 从标准输入读取并转换编码：
   ```bash
   iconv -f UTF-8 -t UTF-16 < input.txt > output.txt
   ```

4. 忽略无法转换的字符：
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
   ```

## 小贴士
- 在转换编码时，确保目标编码支持源文件中的所有字符，以避免数据丢失。
- 使用 `-o` 选项可以直接指定输出文件，避免在终端中显示大量内容。
- 可以使用 `iconv -l` 命令查看支持的编码列表，帮助选择合适的编码格式。