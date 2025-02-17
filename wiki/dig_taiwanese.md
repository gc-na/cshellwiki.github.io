# [Linux] Bash dig 使用法: 查詢 DNS 記錄

## Overview
`dig`（Domain Information Groper）是一個用於查詢 DNS（域名系統）記錄的命令行工具。它可以幫助用戶獲取有關域名的詳細信息，包括 A 記錄、MX 記錄、CNAME 記錄等。

## Usage
基本語法如下：
```
dig [選項] [參數]
```

## Common Options
- `@server`：指定要查詢的 DNS 伺服器。
- `-t type`：指定查詢的記錄類型，例如 A、MX、CNAME 等。
- `+short`：僅顯示簡短的結果，去除多餘的詳細信息。
- `-x`：執行反向查詢，根據 IP 地址查找對應的域名。

## Common Examples
以下是一些常見的 `dig` 使用範例：

1. 查詢 A 記錄：
   ```bash
   dig example.com
   ```

2. 查詢 MX 記錄：
   ```bash
   dig -t MX example.com
   ```

3. 使用指定的 DNS 伺服器查詢：
   ```bash
   dig @8.8.8.8 example.com
   ```

4. 獲取簡短的查詢結果：
   ```bash
   dig +short example.com
   ```

5. 反向查詢 IP 地址：
   ```bash
   dig -x 8.8.8.8
   ```

## Tips
- 使用 `+short` 選項可以快速獲得簡潔的結果，特別是在只需要基本信息時。
- 如果你經常查詢某個域名，可以將查詢結果保存到文件中，以便日後參考。
- 嘗試不同的 DNS 伺服器（如 Google 的 8.8.8.8 或 Cloudflare 的 1.1.1.1）來比較查詢結果的差異。