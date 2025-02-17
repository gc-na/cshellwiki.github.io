# [Linux] Bash systemctl 使用法: 管理系統服務

## Overview
`systemctl` 是一個用於管理 Linux 系統服務的命令。它可以啟動、停止、重啟和檢查服務的狀態，並且能夠管理系統的啟動過程。

## Usage
基本語法如下：
```bash
systemctl [options] [arguments]
```

## Common Options
- `start`: 啟動指定的服務。
- `stop`: 停止指定的服務。
- `restart`: 重啟指定的服務。
- `status`: 顯示指定服務的當前狀態。
- `enable`: 設定服務在系統啟動時自動啟動。
- `disable`: 禁用服務在系統啟動時自動啟動。

## Common Examples
- 啟動服務：
  ```bash
  systemctl start nginx
  ```
  
- 停止服務：
  ```bash
  systemctl stop nginx
  ```

- 重啟服務：
  ```bash
  systemctl restart nginx
  ```

- 檢查服務狀態：
  ```bash
  systemctl status nginx
  ```

- 設定服務自動啟動：
  ```bash
  systemctl enable nginx
  ```

- 禁用服務自動啟動：
  ```bash
  systemctl disable nginx
  ```

## Tips
- 使用 `systemctl list-units --type=service` 可以查看所有服務的列表及其狀態。
- 確保以 root 權限執行 `systemctl` 命令，以避免權限問題。
- 使用 `journalctl -u [service]` 可以查看特定服務的日誌，幫助排除故障。