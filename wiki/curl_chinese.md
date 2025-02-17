# [Linux] Bash curl 用法：用于数据传输的命令行工具

## 概述
curl 是一个用于从或向服务器传输数据的命令行工具。它支持多种协议，包括 HTTP、HTTPS、FTP 等，广泛用于下载文件、发送 API 请求等。

## 用法
curl 的基本语法如下：
```bash
curl [options] [arguments]
```

## 常用选项
- `-X`：指定请求方法（如 GET、POST）。
- `-d`：发送数据（通常用于 POST 请求）。
- `-H`：添加 HTTP 头部信息。
- `-o`：将输出保存到文件。
- `-I`：仅获取 HTTP 头部信息。
- `-L`：跟随重定向。

## 常见示例
1. **下载文件**
   ```bash
   curl -O https://example.com/file.zip
   ```

2. **发送 GET 请求**
   ```bash
   curl https://api.example.com/data
   ```

3. **发送 POST 请求**
   ```bash
   curl -X POST -d "name=John&age=30" https://api.example.com/users
   ```

4. **添加自定义头部**
   ```bash
   curl -H "Authorization: Bearer token" https://api.example.com/protected
   ```

5. **获取 HTTP 头部信息**
   ```bash
   curl -I https://example.com
   ```

## 提示
- 使用 `-L` 选项可以确保 curl 跟随重定向，避免下载失败。
- 在处理敏感数据时，确保使用 HTTPS 协议以加密传输。
- 使用 `-o` 选项保存输出时，确保文件名是唯一的，以免覆盖已有文件。