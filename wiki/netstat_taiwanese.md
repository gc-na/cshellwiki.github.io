# [台灣] Bash netstat 使用方法: 檢查網路連線狀態

## Overview
`netstat` 是一個用於顯示網路連線、路由表和網路介面統計資訊的命令。它可以幫助使用者了解系統的網路狀態，並診斷網路問題。

## Usage
基本語法如下：
```bash
netstat [options] [arguments]
```

## Common Options
- `-a`: 顯示所有連線和監聽的端口。
- `-t`: 只顯示 TCP 連線。
- `-u`: 只顯示 UDP 連線。
- `-n`: 以數字格式顯示地址和端口號，避免解析主機名稱。
- `-l`: 只顯示正在監聽的服務。
- `-p`: 顯示每個連線所屬的程序名稱。

## Common Examples
1. 顯示所有連線和監聽的端口：
   ```bash
   netstat -a
   ```

2. 顯示所有 TCP 連線：
   ```bash
   netstat -t
   ```

3. 顯示所有 UDP 連線：
   ```bash
   netstat -u
   ```

4. 顯示正在監聽的端口：
   ```bash
   netstat -l
   ```

5. 顯示連線的程序名稱：
   ```bash
   netstat -p
   ```

6. 結合多個選項，例如顯示所有 TCP 連線及其程序名稱：
   ```bash
   netstat -tp
   ```

## Tips
- 使用 `-n` 選項可以加快顯示速度，特別是在網路連線數量較多時。
- 定期檢查網路連線狀態可以幫助及早發現潛在的安全問題。
- 結合 `grep` 命令，可以過濾出特定的連線資訊，例如：
  ```bash
  netstat -an | grep 80
  ```