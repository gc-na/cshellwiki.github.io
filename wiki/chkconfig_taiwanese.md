# [Linux] Bash chkconfig 使用法: 管理系統服務的啟動與關閉

## Overview
`chkconfig` 是一個用於管理 Linux 系統中服務啟動和關閉的命令。它可以讓使用者設定哪些服務在系統啟動時自動啟動，並且可以輕鬆地啟用或停用這些服務。

## Usage
基本語法如下：
```
chkconfig [options] [arguments]
```

## Common Options
- `--list`：列出所有服務的啟動狀態。
- `--add`：將一個新的服務添加到 chkconfig 管理中。
- `--del`：從 chkconfig 中刪除一個服務。
- `--level`：指定服務在啟動時的運行級別（例如 2、3、4、5）。
- `on`：啟用服務。
- `off`：停用服務。

## Common Examples
- 列出所有服務及其啟動狀態：
  ```bash
  chkconfig --list
  ```

- 啟用某個服務（例如 `httpd`）：
  ```bash
  chkconfig httpd on
  ```

- 停用某個服務（例如 `ftp`）：
  ```bash
  chkconfig ftp off
  ```

- 添加一個新的服務（例如 `my_service`）：
  ```bash
  chkconfig --add my_service
  ```

- 刪除一個服務（例如 `my_service`）：
  ```bash
  chkconfig --del my_service
  ```

## Tips
- 在修改服務狀態之前，建議先使用 `chkconfig --list` 檢查當前服務的狀態。
- 確保在修改服務設定後，重新啟動系統以確認變更生效。
- 使用 `--level` 參數可以更精確地控制服務在不同運行級別的啟動狀態。