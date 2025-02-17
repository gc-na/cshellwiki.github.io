# [Linux] Bash yes 用法: 持续输出指定字符串

## Overview
`yes` 命令用于持续输出指定的字符串，默认情况下，它会不断输出 "y"。这个命令常用于自动化脚本中，以提供确认输入。

## Usage
基本语法如下：
```bash
yes [options] [arguments]
```

## Common Options
- `-h`, `--help`：显示帮助信息。
- `-V`, `--version`：显示版本信息。

## Common Examples
以下是一些常见的使用示例：

1. **输出默认字符串 "y"**：
   ```bash
   yes
   ```

2. **输出自定义字符串**：
   ```bash
   yes "继续吗？"
   ```

3. **将输出重定向到文件**：
   ```bash
   yes "确认" > confirmation.txt
   ```

4. **与其他命令结合使用**：
   ```bash
   yes | rm -i *.tmp
   ```

## Tips
- 使用 `yes` 时要小心，因为它会无限输出，可能会导致终端被淹没。
- 可以使用 `head` 命令限制输出行数，例如：
  ```bash
  yes "确认" | head -n 5
  ```
- 在需要自动确认的脚本中，`yes` 是一个非常有用的工具，可以节省手动输入的时间。