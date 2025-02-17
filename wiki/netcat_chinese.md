# [Linux] Bash netcat 用法: 网络工具

## 概述
netcat（通常称为“nc”）是一个功能强大的网络工具，可以用来读写网络连接上的数据。它支持多种协议，包括 TCP 和 UDP，常用于调试和网络服务的测试。

## 用法
基本语法如下：
```bash
netcat [选项] [参数]
```

## 常用选项
- `-l`：监听模式，等待连接。
- `-p`：指定端口号。
- `-u`：使用 UDP 协议。
- `-v`：详细模式，输出更多信息。
- `-z`：扫描模式，不发送数据，只进行连接测试。

## 常见示例
1. **建立 TCP 连接**
   ```bash
   netcat example.com 80
   ```
   连接到 `example.com` 的 80 端口。

2. **监听指定端口**
   ```bash
   netcat -l -p 1234
   ```
   在本地机器上监听 1234 端口，等待连接。

3. **发送文件**
   ```bash
   netcat -l -p 1234 > received_file.txt
   ```
   在 1234 端口监听并将接收到的数据保存为 `received_file.txt`。

4. **使用 UDP 发送数据**
   ```bash
   echo "Hello, World!" | netcat -u -w1 example.com 1234
   ```
   通过 UDP 向 `example.com` 的 1234 端口发送 "Hello, World!"。

5. **端口扫描**
   ```bash
   netcat -z -v example.com 1-1000
   ```
   扫描 `example.com` 的 1 到 1000 端口，检查哪些端口开放。

## 小贴士
- 使用 `-v` 选项可以帮助你调试连接问题，提供更多信息。
- 在使用监听模式时，确保没有其他服务占用相同的端口。
- netcat 可以与其他命令结合使用，例如通过管道将数据传输到其他程序。