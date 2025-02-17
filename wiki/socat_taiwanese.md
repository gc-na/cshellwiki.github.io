# [Linux] Bash socat 使用法: 用於網路連接和數據轉發的工具

## Overview
`socat` 是一個強大的網路工具，用於在不同的數據流之間建立雙向連接。它能夠處理多種協議和數據類型，並且常用於網路調試、數據轉發及建立虛擬串口等場景。

## Usage
基本語法如下：
```
socat [options] [arguments]
```

## Common Options
- `-u`: 使用無連接模式。
- `-v`: 顯示詳細的輸出，便於調試。
- `tcp:<host>:<port>`: 連接到指定的 TCP 主機和端口。
- `udp:<host>:<port>`: 連接到指定的 UDP 主機和端口。
- `pty`: 創建一個虛擬終端設備。

## Common Examples
以下是一些常見的 `socat` 使用範例：

1. **建立一個 TCP 伺服器**
   ```bash
   socat TCP-LISTEN:1234,fork EXEC:/bin/bash
   ```
   這將在端口 1234 上啟動一個 TCP 伺服器，並在每個連接上執行一個 bash shell。

2. **將本地端口轉發到遠端伺服器**
   ```bash
   socat TCP-LISTEN:8080,fork TCP:example.com:80
   ```
   此命令將本地的 8080 端口轉發到 `example.com` 的 80 端口。

3. **創建虛擬串口**
   ```bash
   socat pty,link=/dev/ttyV0,mode=777 pty,link=/dev/ttyV1,mode=777
   ```
   這將創建兩個虛擬串口，分別為 `/dev/ttyV0` 和 `/dev/ttyV1`。

4. **UDP 數據轉發**
   ```bash
   socat UDP-LISTEN:1234,fork UDP:example.com:1234
   ```
   此命令會在本地的 1234 端口上接收 UDP 數據，並轉發到 `example.com` 的 1234 端口。

## Tips
- 使用 `-v` 選項可以幫助你在調試時獲得更多的輸出信息。
- 當使用 TCP 伺服器時，`fork` 選項可以讓伺服器同時處理多個連接。
- 確保你有適當的權限來訪問所需的端口，特別是在使用低號端口時。