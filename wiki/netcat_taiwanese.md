# [台灣] Bash netcat 使用方式: 網路連接工具

## Overview
netcat（通常簡稱為 nc）是一個功能強大的網路工具，可以用來讀取和寫入網路連接，支援 TCP 和 UDP 協議。它常被用來進行網路調試、傳輸檔案和建立簡單的伺服器。

## Usage
基本語法如下：

```
netcat [選項] [參數]
```

## Common Options
- `-l`：在伺服器模式下運行，等待連接。
- `-p`：指定本地端口。
- `-u`：使用 UDP 而不是 TCP。
- `-v`：啟用詳細模式，顯示更多的運行信息。
- `-z`：掃描模式，僅檢查端口是否開放。

## Common Examples

1. **建立一個簡單的 TCP 伺服器**
   ```bash
   nc -l -p 1234
   ```
   這會在本地的 1234 端口上啟動一個伺服器，等待客戶端連接。

2. **連接到一個 TCP 伺服器**
   ```bash
   nc example.com 80
   ```
   這會連接到 `example.com` 的 80 端口，通常用於 HTTP 請求。

3. **傳輸檔案**
   在伺服器端：
   ```bash
   nc -l -p 1234 > received_file.txt
   ```
   在客戶端：
   ```bash
   nc server_ip 1234 < file_to_send.txt
   ```
   這會將 `file_to_send.txt` 檔案傳輸到伺服器端並儲存為 `received_file.txt`。

4. **掃描開放的端口**
   ```bash
   nc -zv example.com 20-30
   ```
   這會掃描 `example.com` 的 20 到 30 端口，並顯示哪些端口是開放的。

## Tips
- 使用 `-v` 選項可以幫助你獲得更多的調試信息，特別是在連接失敗時。
- 當使用 `-l` 選項時，確保指定的端口沒有被其他應用佔用。
- netcat 是一個非常靈活的工具，能夠用於多種網路任務，建議多加練習以熟悉其功能。