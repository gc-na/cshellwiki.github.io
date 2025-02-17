# [Linux] Bash traceroute6 使用方式: 用於追蹤 IPv6 網路路徑

## Overview
`traceroute6` 是一個用於追蹤 IPv6 網路路徑的命令。它可以顯示從本地系統到目標主機之間的路由器（跳點），幫助用戶了解網路連接的狀況和延遲。

## Usage
基本語法如下：
```bash
traceroute6 [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: 設定最大跳數（TTL）。
- `-p <port>`: 指定要使用的目的端口。
- `-w <timeout>`: 設定每個回應的超時時間（秒）。
- `-q <nqueries>`: 設定每個跳點發送的查詢數量。

## Common Examples
1. 基本使用，追蹤到一個 IPv6 地址：
   ```bash
   traceroute6 2001:4860:4860::8888
   ```

2. 設定最大跳數為 20：
   ```bash
   traceroute6 -m 20 2001:4860:4860::8888
   ```

3. 指定目的端口為 80（HTTP）：
   ```bash
   traceroute6 -p 80 2001:4860:4860::8888
   ```

4. 設定超時時間為 2 秒：
   ```bash
   traceroute6 -w 2 2001:4860:4860::8888
   ```

5. 每個跳點發送 3 次查詢：
   ```bash
   traceroute6 -q 3 2001:4860:4860::8888
   ```

## Tips
- 使用 `-m` 選項可以避免查詢過多的跳點，特別是在大型網路中。
- 當追蹤的目標無法連接時，檢查防火牆設定，可能會影響結果。
- 結合 `-p` 選項可以幫助診斷特定服務的可達性。