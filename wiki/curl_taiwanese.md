# [Linux] Bash curl 使用法: 用於傳輸數據的工具

## Overview
`curl` 是一個用於從網絡上傳輸數據的命令行工具。它支持多種協議，包括 HTTP、HTTPS、FTP 等，並且可以用於發送請求和接收響應，廣泛應用於 API 測試和文件下載。

## Usage
基本語法如下：
```
curl [options] [arguments]
```

## Common Options
- `-X, --request <command>`: 指定要使用的 HTTP 方法，例如 GET、POST。
- `-d, --data <data>`: 發送數據，通常用於 POST 請求。
- `-H, --header <header>`: 添加自定義的 HTTP 標頭。
- `-o, --output <file>`: 將響應內容寫入指定的文件。
- `-I, --head`: 只獲取 HTTP 標頭，不下載內容。

## Common Examples
1. **發送 GET 請求**
   ```bash
   curl https://api.example.com/data
   ```

2. **發送 POST 請求**
   ```bash
   curl -X POST -d "name=John&age=30" https://api.example.com/users
   ```

3. **添加自定義標頭**
   ```bash
   curl -H "Authorization: Bearer token" https://api.example.com/protected
   ```

4. **下載文件**
   ```bash
   curl -o myfile.zip https://example.com/file.zip
   ```

5. **獲取 HTTP 標頭**
   ```bash
   curl -I https://api.example.com
   ```

## Tips
- 使用 `-L` 選項來自動跟隨重定向。
- 結合 `-o` 和 `-L` 可以方便地下載重定向的文件。
- 使用 `-v` 選項可以查看詳細的請求和響應過程，對於調試非常有幫助。