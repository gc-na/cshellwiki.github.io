# [Linux] Bash echo 用法: 输出文本或变量的值

## 概述
`echo` 命令用于在终端上输出文本或变量的值。它是 Bash 中最常用的命令之一，通常用于显示信息或调试脚本。

## 用法
基本语法如下：
```bash
echo [选项] [参数]
```

## 常用选项
- `-n`：不输出结尾的换行符。
- `-e`：启用转义字符，例如 `\n`（换行）、`\t`（制表符）。
- `-E`：禁用转义字符（默认行为）。

## 常见示例
1. 输出简单文本：
   ```bash
   echo "Hello, World!"
   ```

2. 输出变量的值：
   ```bash
   name="Alice"
   echo "My name is $name."
   ```

3. 使用 `-n` 选项输出不换行：
   ```bash
   echo -n "This is a single line."
   ```

4. 使用 `-e` 选项输出带有转义字符的文本：
   ```bash
   echo -e "Line 1\nLine 2"
   ```

5. 输出当前日期和时间：
   ```bash
   echo "Current date and time: $(date)"
   ```

## 提示
- 使用双引号包围文本可以确保变量被正确解析。
- 在脚本中使用 `echo` 时，可以结合其他命令使用管道（|）来处理输出。
- 注意在输出敏感信息时，避免泄露环境变量的内容。