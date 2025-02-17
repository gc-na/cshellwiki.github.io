# [Linux] Bash journalctl 使用說明: 查看系統日誌

## Overview
`journalctl` 是一個用於查詢和顯示系統日誌的命令。它可以從 systemd 日誌中檢索和顯示各種服務和系統事件的詳細信息，幫助用戶進行故障排除和監控系統狀態。

## Usage
基本語法如下：
```
journalctl [options] [arguments]
```

## Common Options
- `-b`：顯示當前啟動以來的日誌。
- `-f`：持續顯示最新的日誌輸出，類似於 `tail -f`。
- `--since`：顯示指定時間以來的日誌，例如 `--since "2023-10-01"`。
- `--until`：顯示直到指定時間的日誌，例如 `--until "2023-10-02"`。
- `-u`：顯示特定服務的日誌，例如 `-u nginx.service`。

## Common Examples
- 查看當前啟動以來的所有日誌：
  ```bash
  journalctl -b
  ```

- 持續顯示最新的日誌：
  ```bash
  journalctl -f
  ```

- 查看特定時間範圍內的日誌：
  ```bash
  journalctl --since "2023-10-01" --until "2023-10-02"
  ```

- 查看特定服務的日誌：
  ```bash
  journalctl -u ssh.service
  ```

- 查看特定優先級的日誌（例如錯誤）：
  ```bash
  journalctl -p err
  ```

## Tips
- 使用 `-n` 選項可以限制顯示的日誌行數，例如 `journalctl -n 100` 只顯示最近的 100 行日誌。
- 結合 `grep` 使用可以更精確地查找特定內容，例如 `journalctl | grep "error"`。
- 定期檢查日誌可以幫助及早發現系統問題，建議將其納入日常維護流程中。