# [Linux] Bash iotop 使用法: 監控磁碟 I/O 活動

## Overview
`iotop` 是一個用於監控系統中磁碟 I/O 活動的命令行工具。它可以顯示當前正在進行的 I/O 操作，並顯示哪些進程正在使用磁碟資源，幫助用戶識別性能瓶頸。

## Usage
基本語法如下：
```bash
iotop [options] [arguments]
```

## Common Options
- `-o` 或 `--only`: 只顯示有 I/O 活動的進程。
- `-b` 或 `--batch`: 以批次模式運行，適合用於腳本。
- `-n NUM`: 指定顯示的更新次數。
- `-d SEC`: 設定更新的間隔時間（秒）。

## Common Examples
1. 以交互模式運行 `iotop`：
   ```bash
   iotop
   ```

2. 只顯示有 I/O 活動的進程：
   ```bash
   iotop -o
   ```

3. 以批次模式運行，並每 5 秒更新一次，顯示 10 次：
   ```bash
   iotop -b -d 5 -n 10
   ```

4. 將輸出結果導出到文件：
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

## Tips
- 在使用 `iotop` 時，確保你有足夠的權限（通常需要 root 權限）來查看所有進程的 I/O 活動。
- 使用 `-o` 選項可以幫助你快速找到正在進行 I/O 操作的進程，這對於性能調試非常有幫助。
- 定期檢查 I/O 活動可以幫助你了解系統性能，並及時發現潛在的問題。