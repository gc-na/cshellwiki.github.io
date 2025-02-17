# [台灣] Bash ping 使用法: 測試網路連接

## Overview
`ping` 命令用於測試與另一台計算機之間的網路連接。它通過發送 ICMP 回音請求來檢查目標主機是否可達，並計算回應時間。

## Usage
基本語法如下：
```
ping [選項] [目標]
```

## Common Options
- `-c [次數]`：指定要發送的請求次數。
- `-i [秒數]`：設置發送請求之間的間隔時間（以秒為單位）。
- `-t [TTL]`：設置傳送的數據包的生存時間（TTL）。
- `-s [大小]`：指定要發送的數據包大小。

## Common Examples
以下是一些常見的 `ping` 使用範例：

1. **基本使用**
   ```bash
   ping google.com
   ```

2. **指定發送次數**
   ```bash
   ping -c 4 google.com
   ```

3. **設置間隔時間**
   ```bash
   ping -i 2 google.com
   ```

4. **指定數據包大小**
   ```bash
   ping -s 100 google.com
   ```

5. **設置TTL**
   ```bash
   ping -t 64 google.com
   ```

## Tips
- 使用 `-c` 選項可以避免 `ping` 命令無限運行，方便進行測試。
- 觀察回應時間可以幫助你了解網路的延遲情況。
- 如果你無法連接到某個網站，嘗試 `ping` 其他網站以確定問題是否出在特定的目標上。