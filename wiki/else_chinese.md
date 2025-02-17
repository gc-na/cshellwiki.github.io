# [Linux] Bash else 用法: 条件语句的选择

## 概述
`else` 命令是 Bash 脚本中的一个条件语句，用于在 `if` 语句的条件不满足时执行特定的命令。它通常与 `if` 语句一起使用，以提供一种控制程序流的方式。

## 用法
基本语法如下：
```bash
if [ condition ]; then
    # 如果条件为真执行的命令
else
    # 如果条件为假执行的命令
fi
```

## 常用选项
`else` 本身没有选项，但它通常与 `if` 语句结合使用。以下是与 `if` 相关的一些常用选项：
- `-eq`：检查两个数是否相等。
- `-ne`：检查两个数是否不相等。
- `-lt`：检查第一个数是否小于第二个数。
- `-gt`：检查第一个数是否大于第二个数。
- `-z`：检查字符串是否为空。

## 常见示例
以下是一些使用 `else` 的实际示例：

### 示例 1：基本的条件判断
```bash
#!/bin/bash
number=10

if [ $number -gt 5 ]; then
    echo "数字大于5"
else
    echo "数字小于或等于5"
fi
```

### 示例 2：检查文件是否存在
```bash
#!/bin/bash
file="example.txt"

if [ -f $file ]; then
    echo "文件存在"
else
    echo "文件不存在"
fi
```

### 示例 3：用户输入验证
```bash
#!/bin/bash
read -p "请输入一个数字: " input

if [ $input -eq 10 ]; then
    echo "你输入的是10"
else
    echo "你输入的不是10"
fi
```

## 提示
- 在使用 `if` 和 `else` 时，确保条件语句的格式正确，避免语法错误。
- 使用 `elif` 可以在多个条件之间进行更复杂的判断。
- 在脚本中使用注释来解释条件的目的，增加可读性。