# [Linux] Bash screen 使用: 管理终端会话

## 概述
`screen` 命令是一个终端多路复用器，它允许用户在一个单一的终端窗口中创建和管理多个会话。用户可以在这些会话之间切换，甚至在断开连接后重新连接，保持工作状态。

## 使用方法
基本语法如下：
```
screen [options] [arguments]
```

## 常用选项
- `-S <session_name>`: 创建一个命名的会话。
- `-d -r <session_name>`: 断开并重新连接到指定的会话。
- `-list`: 列出所有当前的会话。
- `-X <command>`: 向指定的会话发送命令。

## 常见示例
1. 创建一个新的会话：
   ```bash
   screen -S mysession
   ```

2. 列出所有会话：
   ```bash
   screen -list
   ```

3. 断开当前会话：
   ```bash
   Ctrl + A, D
   ```

4. 重新连接到一个会话：
   ```bash
   screen -r mysession
   ```

5. 向会话发送命令：
   ```bash
   screen -S mysession -X stuff "echo Hello World\n"
   ```

## 小贴士
- 使用命名会话可以更方便地管理多个会话。
- 定期保存你的工作，以防止意外断开连接。
- 可以使用 `Ctrl + A` 然后按 `?` 查看所有快捷键帮助。