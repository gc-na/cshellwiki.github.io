# [Linux] Bash trap 用法: 捕获信号和清理资源

## 概述
`trap` 命令用于捕获和处理信号，允许用户在脚本接收到特定信号时执行清理操作或其他命令。这在处理脚本的中断、退出或错误时非常有用。

## 用法
基本语法如下：
```bash
trap [options] [commands] [signals]
```

## 常用选项
- `-l`：列出所有可用的信号名称。
- `-p`：打印当前的 trap 设置。
- `signals`：指定要捕获的信号，例如 `SIGINT`、`SIGTERM` 等。

## 常见示例
1. **捕获 SIGINT 信号**
   ```bash
   trap 'echo "脚本被中断"; exit' SIGINT
   while true; do
       echo "运行中..."
       sleep 1
   done
   ```

2. **在脚本退出时清理临时文件**
   ```bash
   trap 'rm -f /tmp/tempfile' EXIT
   touch /tmp/tempfile
   echo "临时文件已创建"
   ```

3. **捕获多个信号**
   ```bash
   trap 'echo "收到信号"; exit' SIGINT SIGTERM
   while true; do
       echo "运行中..."
       sleep 1
   done
   ```

## 提示
- 在使用 `trap` 时，确保清理操作是必要的，以避免不必要的资源浪费。
- 使用 `trap` 捕获信号时，考虑到脚本的可读性和维护性，尽量保持代码简洁。
- 在调试脚本时，可以使用 `trap -p` 查看当前的 trap 设置，帮助你理解信号处理的状态。