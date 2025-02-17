# [台灣] Bash traceroute 使用法: 追蹤網路路徑

## Overview
`traceroute` 是一個用於顯示資料包在網路中從源頭到目的地的路徑的命令。它能幫助用戶了解資料在網路中傳輸的過程，並識別可能的延遲或問題點。

## Usage
基本語法如下：
```bash
traceroute [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: 設定最大生存時間（TTL），預設為30。
- `-n`: 直接使用IP地址而不解析主機名稱。
- `-p <port>`: 指定目標主機的端口，預設為33434。
- `-w <timeout>`: 設定每個回應的超時時間，預設為5秒。

## Common Examples
1. 基本使用，追蹤到某個網站的路徑：
   ```bash
   traceroute example.com
   ```

2. 使用數字格式顯示IP地址：
   ```bash
   traceroute -n example.com
   ```

3. 設定最大TTL為15：
   ```bash
   traceroute -m 15 example.com
   ```

4. 指定端口號進行追蹤：
   ```bash
   traceroute -p 80 example.com
   ```

5. 設定超時時間為2秒：
   ```bash
   traceroute -w 2 example.com
   ```

## Tips
- 在進行網路故障排除時，使用 `-n` 選項可以加快顯示速度，因為不需要進行DNS查詢。
- 如果你發現某個跳點的延遲特別高，可以進一步檢查該節點的狀態。
- 在防火牆或路由器上，某些ICMP封包可能會被阻擋，這可能會影響 `traceroute` 的結果。