# [Linux] Bash tcpdump 使用方法: 捕获网络数据包

## 概述
tcpdump 是一个强大的命令行工具，用于捕获和分析网络流量。它可以帮助用户监控网络活动，调试网络问题，以及进行安全分析。

## 用法
tcpdump 的基本语法如下：

```bash
tcpdump [options] [arguments]
```

## 常用选项
- `-i <interface>`: 指定要监听的网络接口。
- `-n`: 不解析主机名，直接显示 IP 地址。
- `-c <count>`: 捕获指定数量的数据包后停止。
- `-w <file>`: 将捕获的数据包写入文件。
- `-r <file>`: 从文件中读取数据包进行分析。
- `-v`, `-vv`, `-vvv`: 增加输出的详细程度。

## 常见示例
1. 捕获所有流量：
   ```bash
   tcpdump
   ```

2. 捕获特定接口上的流量：
   ```bash
   tcpdump -i eth0
   ```

3. 捕获指定数量的数据包：
   ```bash
   tcpdump -c 10
   ```

4. 将捕获的数据包保存到文件：
   ```bash
   tcpdump -w capture.pcap
   ```

5. 从文件中读取并分析数据包：
   ```bash
   tcpdump -r capture.pcap
   ```

6. 捕获特定端口的流量（例如，HTTP 流量）：
   ```bash
   tcpdump -i eth0 port 80
   ```

## 小贴士
- 在使用 tcpdump 时，建议以 root 用户身份运行，以确保能够捕获所有数据包。
- 使用 `-n` 选项可以加快捕获速度，因为它避免了 DNS 查询。
- 捕获的数据包文件可以使用 Wireshark 等图形化工具进行进一步分析。
- 定期清理旧的捕获文件，以节省存储空间。