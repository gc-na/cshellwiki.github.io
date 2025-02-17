# [Linux] Bash sftp 使用方法: 进行安全文件传输

## 概述
`sftp`（SSH 文件传输协议）是一种安全的网络协议，用于在计算机之间传输文件。它通过 SSH（安全外壳协议）提供加密的文件传输功能，确保数据在传输过程中的安全性。

## 用法
基本语法如下：
```
sftp [选项] [用户@主机]
```

## 常用选项
- `-P`：指定端口号。
- `-o`：传递选项，例如 `-oPort=2222`。
- `-b`：使用批处理模式，从文件中读取命令。
- `-v`：启用详细模式，显示调试信息。

## 常见示例
1. 连接到远程服务器：
   ```bash
   sftp user@hostname
   ```

2. 指定端口连接：
   ```bash
   sftp -P 2222 user@hostname
   ```

3. 从远程服务器下载文件：
   ```bash
   sftp user@hostname:/remote/path/file.txt /local/path/
   ```

4. 上传文件到远程服务器：
   ```bash
   sftp user@hostname
   put /local/path/file.txt /remote/path/
   ```

5. 列出远程目录中的文件：
   ```bash
   sftp user@hostname
   ls /remote/path/
   ```

## 提示
- 使用 `-v` 选项可以帮助你调试连接问题。
- 在使用 `put` 或 `get` 命令时，可以使用通配符来选择多个文件。
- 定期检查和更新 SSH 密钥，以确保连接的安全性。