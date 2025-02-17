# [Linux] Bash awk 用法: 文本处理工具

## 概述
`awk` 是一种强大的文本处理工具，主要用于模式扫描和处理。它可以对文本文件中的数据进行分析、提取和格式化，广泛应用于数据报告和数据处理任务。

## 用法
基本语法如下：
```bash
awk [options] 'pattern { action }' [file...]
```

## 常用选项
- `-F`：指定输入字段分隔符。
- `-v`：定义变量。
- `-f`：从文件中读取 awk 程序。
- `-e`：直接在命令行中指定 awk 程序。

## 常见示例
1. **打印文件的第一列**
   ```bash
   awk '{print $1}' filename.txt
   ```

2. **使用特定分隔符（如逗号）打印第二列**
   ```bash
   awk -F',' '{print $2}' filename.csv
   ```

3. **计算文件中数字的总和**
   ```bash
   awk '{sum += $1} END {print sum}' numbers.txt
   ```

4. **筛选出大于50的数字**
   ```bash
   awk '$1 > 50' numbers.txt
   ```

5. **从文件中提取特定模式的行**
   ```bash
   awk '/pattern/' filename.txt
   ```

## 提示
- 使用 `-F` 选项时，确保分隔符与文件格式一致。
- 可以通过 `BEGIN` 和 `END` 块来处理文件的开始和结束。
- 在处理大文件时，尽量使用 `awk` 的内置变量和函数，以提高效率。