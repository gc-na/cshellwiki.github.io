# [Linux] Bash dnf 使用方式: 管理和安裝軟體包

## Overview
`dnf`（Dandified YUM）是一個用於管理和安裝Linux系統上軟體包的命令行工具。它是YUM的下一代版本，提供了更快的性能和更好的依賴性解決方案。

## Usage
基本語法如下：
```
dnf [options] [arguments]
```

## Common Options
- `install`: 安裝指定的軟體包。
- `remove`: 移除已安裝的軟體包。
- `update`: 更新已安裝的軟體包到最新版本。
- `search`: 搜尋可用的軟體包。
- `info`: 顯示指定軟體包的詳細資訊。

## Common Examples
- 安裝軟體包：
  ```bash
  dnf install package_name
  ```
- 移除軟體包：
  ```bash
  dnf remove package_name
  ```
- 更新所有已安裝的軟體包：
  ```bash
  dnf update
  ```
- 搜尋軟體包：
  ```bash
  dnf search package_name
  ```
- 顯示軟體包資訊：
  ```bash
  dnf info package_name
  ```

## Tips
- 在執行更新之前，建議先使用 `dnf check-update` 來查看可用的更新。
- 使用 `dnf history` 可以查看過去的操作紀錄，方便追蹤變更。
- 在安裝軟體包時，可以使用 `-y` 選項自動確認安裝，避免手動確認的步驟。