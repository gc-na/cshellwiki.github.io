# [Linux] Bash test 用法: 测试文件和字符串的条件

## 概述
`test` 命令用于评估条件表达式，通常用于脚本中判断文件属性、字符串比较和数值比较。它返回一个状态码，表示条件是否为真（0 表示真，1 表示假）。

## 用法
基本语法如下：
```bash
test [选项] [参数]
```

## 常用选项
- `-e 文件`：检查文件是否存在。
- `-f 文件`：检查文件是否为常规文件。
- `-d 文件`：检查文件是否为目录。
- `-s 文件`：检查文件是否非空。
- `字符串1 = 字符串2`：检查两个字符串是否相等。
- `整数1 -eq 整数2`：检查两个整数是否相等。

## 常见示例
以下是一些常见的 `test` 命令使用示例：

### 示例 1: 检查文件是否存在
```bash
if test -e myfile.txt; then
    echo "文件存在"
else
    echo "文件不存在"
fi
```

### 示例 2: 检查是否为目录
```bash
if test -d /home/user; then
    echo "这是一个目录"
else
    echo "这不是一个目录"
fi
```

### 示例 3: 字符串比较
```bash
str1="hello"
str2="world"
if test "$str1" = "$str2"; then
    echo "字符串相等"
else
    echo "字符串不相等"
fi
```

### 示例 4: 数值比较
```bash
num1=10
num2=20
if test $num1 -lt $num2; then
    echo "$num1 小于 $num2"
else
    echo "$num1 不小于 $num2"
fi
```

## 提示
- 使用 `[` 和 `]` 作为 `test` 的替代形式，例如 `[ -e myfile.txt ]`，这在 Bash 脚本中更为常见。
- 在字符串比较时，确保使用双引号以避免空字符串引发错误。
- 结合 `&&` 和 `||` 可以实现更复杂的条件判断，例如：
  ```bash
  test -e myfile.txt && echo "文件存在" || echo "文件不存在"
  ```