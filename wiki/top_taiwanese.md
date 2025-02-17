# [Linux] Bash top 使用法: 監控系統資源使用情況

## Overview
`top` 命令是一個用於實時顯示系統中運行的進程及其資源使用情況的工具。它提供了 CPU、記憶體和其他系統資源的即時狀態，幫助用戶了解系統性能。

## Usage
基本語法如下：
```bash
top [options] [arguments]
```

## Common Options
- `-d <seconds>`: 設定更新間隔時間（以秒為單位）。
- `-n <number>`: 指定顯示的更新次數。
- `-p <pid>`: 只顯示指定進程 ID 的進程。
- `-u <user>`: 只顯示特定用戶的進程。

## Common Examples
1. **啟動 top 命令**
   ```bash
   top
   ```

2. **每 2 秒更新一次**
   ```bash
   top -d 2
   ```

3. **顯示特定進程 ID（例如 PID 1234）**
   ```bash
   top -p 1234
   ```

4. **顯示特定用戶（例如 user1）的進程**
   ```bash
   top -u user1
   ```

5. **顯示 5 次更新後自動退出**
   ```bash
   top -n 5
   ```

## Tips
- 使用 `Shift + M` 可以根據記憶體使用量排序進程。
- 使用 `Shift + P` 可以根據 CPU 使用量排序進程。
- 按 `q` 鍵可以快速退出 `top` 界面。
- 定期檢查系統資源使用情況，及時發現並解決性能瓶頸。