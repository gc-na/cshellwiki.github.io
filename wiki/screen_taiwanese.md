# [Linux] Bash screen 使用法: 管理多個終端會話

## Overview
`screen` 是一個終端多工工具，允許用戶在單一終端窗口中創建和管理多個會話。這對於需要長時間運行的任務特別有用，因為即使用戶斷開連接，這些會話仍然可以在背景中繼續運行。

## Usage
基本語法如下：
```
screen [options] [arguments]
```

## Common Options
- `-S <session_name>`: 指定會話名稱，方便識別和管理。
- `-d -r <session_name>`: 斷開並重新連接到指定的會話。
- `-list`: 列出當前所有的 screen 會話。
- `-L`: 啟用日誌記錄，將會話輸出保存到文件中。

## Common Examples
- 創建一個新的 screen 會話：
  ```bash
  screen -S mysession
  ```

- 斷開當前的 screen 會話（保持會話在背景中運行）：
  ```bash
  Ctrl + A, D
  ```

- 列出所有的 screen 會話：
  ```bash
  screen -list
  ```

- 重新連接到一個已存在的會話：
  ```bash
  screen -r mysession
  ```

- 啟用日誌記錄並創建會話：
  ```bash
  screen -L -S logging_session
  ```

## Tips
- 使用有意義的會話名稱，以便於管理和識別。
- 定期檢查和清理不再需要的會話，以保持系統整潔。
- 在長時間運行的任務中使用日誌記錄功能，以便後續查看輸出。