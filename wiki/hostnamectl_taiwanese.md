# [Linux] Bash hostnamectl 使用法: 管理系統主機名稱

## Overview
`hostnamectl` 是一個用於管理和查詢系統主機名稱的命令。它可以讓使用者輕鬆地設定主機名稱、顯示當前主機名稱以及管理其他與主機相關的資訊。

## Usage
基本語法如下：
```
hostnamectl [options] [arguments]
```

## Common Options
- `set-hostname`: 設定新的主機名稱。
- `status`: 顯示當前主機名稱及其他相關資訊。
- `set-icon-name`: 設定主機的圖示名稱。
- `set-chassis`: 設定主機的類型（如桌面、伺服器等）。

## Common Examples
- **顯示當前主機名稱**
  ```bash
  hostnamectl status
  ```

- **設定新的主機名稱**
  ```bash
  sudo hostnamectl set-hostname 新的主機名稱
  ```

- **設定主機的圖示名稱**
  ```bash
  sudo hostnamectl set-icon-name my-icon
  ```

- **設定主機類型為伺服器**
  ```bash
  sudo hostnamectl set-chassis server
  ```

## Tips
- 在設定主機名稱後，建議重啟系統以確保所有服務都能識別新的主機名稱。
- 使用 `sudo` 執行命令，以獲得必要的權限來修改主機名稱。
- 確保新的主機名稱符合系統的命名規則，避免使用特殊字符。