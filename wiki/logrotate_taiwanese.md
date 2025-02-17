# [Linux] Bash logrotate 用法: 管理日誌檔案的輪替

## Overview
logrotate 是一個用於管理系統日誌檔案的工具，能夠自動輪替、壓縮、刪除和郵寄日誌檔案，以確保系統不會因為日誌檔案過大而影響性能。

## Usage
基本語法如下：
```bash
logrotate [options] [arguments]
```

## Common Options
- `-f`：強制執行日誌輪替，即使沒有達到設定的條件。
- `-s`：指定狀態檔案的路徑，該檔案用來記錄上次輪替的狀態。
- `-d`：以偵錯模式運行，顯示將要執行的操作，但不實際執行。
- `-v`：顯示詳細的執行過程。

## Common Examples
以下是一些常見的使用範例：

1. **手動執行日誌輪替**
   ```bash
   logrotate -f /etc/logrotate.conf
   ```

2. **使用狀態檔案**
   ```bash
   logrotate -s /var/lib/logrotate/status /etc/logrotate.conf
   ```

3. **偵錯模式運行**
   ```bash
   logrotate -d /etc/logrotate.conf
   ```

4. **顯示詳細執行過程**
   ```bash
   logrotate -v /etc/logrotate.conf
   ```

## Tips
- 定期檢查 logrotate 的設定檔，以確保日誌檔案的管理符合需求。
- 使用 `-d` 選項進行偵錯，這樣可以在實際執行之前預覽將要進行的操作。
- 確保日誌檔案的擁有者和權限正確，以避免因權限問題導致的輪替失敗。