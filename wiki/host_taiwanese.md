# [Linux] Bash host 使用法: 查詢 DNS 資訊

## Overview
`host` 是一個用於查詢 DNS（域名系統）資訊的命令。它可以幫助用戶獲取有關域名的詳細資料，包括 IP 地址、郵件交換器等。

## Usage
基本語法如下：
```
host [選項] [域名]
```

## Common Options
- `-a`：查詢所有資訊，包括 A、MX 和 TXT 紀錄。
- `-t [類型]`：指定查詢的紀錄類型，例如 A、MX、TXT 等。
- `-v`：啟用詳細模式，顯示更多的查詢過程資訊。

## Common Examples
查詢某個域名的 IP 地址：
```bash
host example.com
```

查詢特定類型的 DNS 紀錄，例如 MX 紀錄：
```bash
host -t MX example.com
```

查詢所有可用的 DNS 紀錄：
```bash
host -a example.com
```

使用自訂的 DNS 伺服器進行查詢：
```bash
host example.com 8.8.8.8
```

## Tips
- 當你需要快速檢查某個域名的 IP 地址時，`host` 是一個非常方便的工具。
- 使用 `-v` 選項可以幫助你了解查詢的過程，對於故障排除特別有用。
- 如果你經常查詢某些域名，可以考慮將常用的命令寫入腳本中，以提高效率。