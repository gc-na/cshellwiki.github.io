# [台灣] Bash iostat 使用法: 監控系統的 I/O 性能

## Overview
`iostat` 是一個用於監控系統 I/O 性能的命令行工具。它可以顯示 CPU 使用率和各個磁碟的 I/O 活動，幫助使用者了解系統的性能瓶頸。

## Usage
基本語法如下：
```bash
iostat [options] [arguments]
```

## Common Options
- `-c`：顯示 CPU 使用率的統計信息。
- `-d`：顯示磁碟的 I/O 活動。
- `-x`：顯示擴展的磁碟統計信息，包括 I/O 等待時間等。
- `-h`：以人類可讀的格式顯示數據。
- `-t`：顯示時間戳。

## Common Examples
1. 顯示 CPU 使用率：
   ```bash
   iostat -c
   ```

2. 顯示所有磁碟的 I/O 活動：
   ```bash
   iostat -d
   ```

3. 顯示擴展的磁碟統計信息：
   ```bash
   iostat -x
   ```

4. 每 2 秒更新一次顯示 CPU 和磁碟的統計信息：
   ```bash
   iostat -c -d 2
   ```

5. 以人類可讀的格式顯示所有磁碟的 I/O 活動：
   ```bash
   iostat -d -h
   ```

## Tips
- 在監控系統性能時，建議將 `iostat` 與其他工具（如 `top` 或 `vmstat`）結合使用，以獲得更全面的系統狀態。
- 使用 `-t` 參數可以幫助你追蹤性能變化的時間點，這對於故障排除非常有用。
- 定期檢查 I/O 性能，特別是在高負載的環境中，可以幫助及早發現潛在的性能問題。