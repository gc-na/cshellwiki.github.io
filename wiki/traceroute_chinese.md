# [Linux] Bash traceroute 用法: 路由跟踪命令

## 概述
`traceroute` 命令用于跟踪数据包在网络中从源主机到目标主机的路径。它可以帮助用户了解网络连接的延迟和各个跳点的状态，从而诊断网络问题。

## 用法
基本语法如下：
```bash
traceroute [options] [arguments]
```

## 常用选项
- `-m <hops>`: 设置最大跳数。
- `-n`: 不进行域名解析，直接显示IP地址。
- `-p <port>`: 指定使用的端口号。
- `-w <seconds>`: 设置等待每个回复的超时时间。

## 常见示例
1. **基本用法**: 跟踪到某个主机的路由。
   ```bash
   traceroute example.com
   ```

2. **限制最大跳数**: 设置最大跳数为10。
   ```bash
   traceroute -m 10 example.com
   ```

3. **不进行域名解析**: 直接显示IP地址。
   ```bash
   traceroute -n example.com
   ```

4. **指定端口**: 使用特定端口进行跟踪。
   ```bash
   traceroute -p 80 example.com
   ```

5. **设置超时时间**: 等待每个回复的超时时间为2秒。
   ```bash
   traceroute -w 2 example.com
   ```

## 提示
- 在进行网络故障排除时，使用 `-n` 选项可以加快输出速度，避免DNS解析的延迟。
- 了解每个跳点的延迟可以帮助识别网络瓶颈。
- 在某些网络环境中，可能会遇到防火墙阻止 `traceroute` 请求，需考虑使用其他工具进行诊断。