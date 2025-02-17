# [Linux] Bash getopts 用法: 解析命令行选项

## 概述
`getopts` 是一个用于解析命令行选项的 Bash 内置命令。它可以帮助脚本处理用户输入的选项和参数，使得脚本更加灵活和易用。

## 用法
基本语法如下：
```bash
getopts [options] [arguments]
```

## 常用选项
- `-a`：用于指定选项的短格式。
- `-o`：用于定义可接受的选项。
- `-l`：用于定义可接受的长格式选项。

## 常见示例

### 示例 1：基本选项解析
```bash
#!/bin/bash
while getopts "ab:c" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B with argument: $OPTARG"
      ;;
    c)
      echo "Option C selected"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```
在这个示例中，脚本解析了选项 `-a`、`-b`（需要参数）和 `-c`。

### 示例 2：处理长选项
```bash
#!/bin/bash
while getopts "a:b:c" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B with argument: $OPTARG"
      ;;
    c)
      echo "Option C selected"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```
可以通过 `--` 来传递长选项，例如 `./script.sh -a -b value -c`。

### 示例 3：使用默认值
```bash
#!/bin/bash
flag_a=false
flag_b="default"

while getopts "ab:" opt; do
  case $opt in
    a)
      flag_a=true
      ;;
    b)
      flag_b=$OPTARG
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done

echo "Flag A: $flag_a"
echo "Flag B: $flag_b"
```
在这个示例中，选项 `-a` 会设置一个布尔值，而 `-b` 可以接受一个参数。

## 提示
- 使用 `getopts` 时，确保选项字符串的格式正确，短选项后面可以跟一个冒号表示需要参数。
- 在处理选项时，使用 `OPTARG` 变量来获取当前选项的参数值。
- 记得在脚本中提供帮助信息，以便用户了解可用的选项。