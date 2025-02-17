# [Linux] Bash dig 用法: 查询DNS信息

## 概述
`dig`（Domain Information Groper）是一个用于查询DNS（域名系统）信息的命令行工具。它可以帮助用户获取域名的解析记录，包括A记录、MX记录、NS记录等，常用于网络故障排除和域名管理。

## 用法
基本语法如下：
```bash
dig [选项] [参数]
```

## 常用选项
- `@server`：指定要查询的DNS服务器。
- `-t type`：指定查询的记录类型（如A、MX、NS等）。
- `+short`：以简短格式输出结果。
- `+trace`：追踪DNS解析过程，显示每一步的查询结果。

## 常见示例
1. 查询某个域名的A记录：
   ```bash
   dig example.com
   ```

2. 查询特定DNS服务器的MX记录：
   ```bash
   dig @8.8.8.8 example.com -t MX
   ```

3. 获取域名的NS记录，并以简短格式输出：
   ```bash
   dig example.com NS +short
   ```

4. 追踪DNS解析过程：
   ```bash
   dig example.com +trace
   ```

## 提示
- 使用`+short`选项可以快速获取简洁的结果，适合快速查看。
- 在进行DNS故障排除时，尝试使用不同的DNS服务器（如Google的8.8.8.8）来验证问题是否与特定服务器有关。
- 结合`-t`选项，可以灵活查询不同类型的DNS记录，帮助更好地理解域名的配置。