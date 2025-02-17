# [台灣] Bash nslookup 使用方法: 查詢域名的IP地址

## Overview
`nslookup` 是一個用於查詢域名系統（DNS）的命令行工具。它可以幫助用戶查找域名對應的IP地址，或是反向查詢IP地址以獲取相應的域名。

## Usage
基本語法如下：
```
nslookup [options] [arguments]
```

## Common Options
- `-type=TYPE`：指定查詢的記錄類型，例如 A、AAAA、CNAME 等。
- `-timeout=SECONDS`：設置查詢超時的時間，默認為 5 秒。
- `-retry=COUNT`：設置查詢重試的次數，默認為 4 次。
- `-debug`：顯示詳細的調試信息。

## Common Examples
以下是一些常見的使用範例：

1. 查詢域名的IP地址：
   ```bash
   nslookup example.com
   ```

2. 查詢特定類型的DNS記錄（例如，CNAME）：
   ```bash
   nslookup -type=CNAME example.com
   ```

3. 反向查詢IP地址以獲取域名：
   ```bash
   nslookup 93.184.216.34
   ```

4. 使用特定的DNS伺服器進行查詢：
   ```bash
   nslookup example.com 8.8.8.8
   ```

## Tips
- 在進行DNS查詢時，使用 `-debug` 選項可以幫助你了解查詢過程中的詳細信息，對於故障排除非常有用。
- 如果你經常查詢某個域名，可以考慮將其結果緩存，以提高查詢效率。
- 確保你使用的DNS伺服器是可靠的，以獲得準確的查詢結果。