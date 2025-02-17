# [Linux] Bash nslookup 用法: 查询域名的IP地址

## 概述
`nslookup` 是一个用于查询域名系统（DNS）记录的命令行工具。它可以帮助用户获取特定域名的IP地址，或反向查询IP地址以获取相关域名信息。

## 用法
基本语法如下：
```
nslookup [选项] [参数]
```

## 常用选项
- `-type=类型`：指定查询的记录类型，如 A、AAAA、MX 等。
- `-timeout=秒数`：设置查询超时时间，单位为秒。
- `-retry=次数`：设置查询失败后的重试次数。
- `-debug`：显示详细的调试信息。

## 常见示例
1. 查询域名的IP地址：
   ```bash
   nslookup example.com
   ```

2. 查询特定类型的DNS记录（例如MX记录）：
   ```bash
   nslookup -type=MX example.com
   ```

3. 使用指定的DNS服务器进行查询：
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. 反向查询IP地址以获取域名：
   ```bash
   nslookup 93.184.216.34
   ```

## 小贴士
- 使用 `-debug` 选项可以帮助您更好地理解DNS查询的过程，特别是在遇到问题时。
- 如果您经常查询某个域名，可以考虑将其添加到脚本中，以便快速获取信息。
- 注意DNS缓存可能会影响查询结果，必要时可以清除本地DNS缓存。