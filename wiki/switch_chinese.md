# [Linux] Bash switch 用法: 切换选项

## 概述
`switch` 命令用于在 Bash 脚本中根据条件选择不同的执行路径。它通常用于处理多个可能的选项，使得脚本更加灵活和易于维护。

## 用法
基本语法如下：
```bash
switch [options] [arguments]
```

## 常用选项
- `-e`：指定一个表达式，只有在表达式为真时才执行后续的命令。
- `-d`：设置默认选项，当没有其他选项匹配时执行。
- `-h`：显示帮助信息。

## 常见示例
以下是一些常见的 `switch` 命令示例：

### 示例 1: 基本用法
```bash
case $1 in
    start)
        echo "Starting the service..."
        ;;
    stop)
        echo "Stopping the service..."
        ;;
    restart)
        echo "Restarting the service..."
        ;;
    *)
        echo "Usage: $0 {start|stop|restart}"
        ;;
esac
```

### 示例 2: 带默认选项
```bash
case $1 in
    hello)
        echo "Hello, World!"
        ;;
    goodbye)
        echo "Goodbye!"
        ;;
    *)
        echo "Please provide a valid option."
        ;;
esac
```

### 示例 3: 多个条件
```bash
case $1 in
    a|A)
        echo "You selected A."
        ;;
    b|B)
        echo "You selected B."
        ;;
    *)
        echo "Invalid selection."
        ;;
esac
```

## 提示
- 确保在每个选项后使用 `;;` 来结束该选项的命令。
- 使用 `*` 作为默认选项可以捕获所有未匹配的输入。
- 适当地使用引号来处理包含空格或特殊字符的选项。