# [Linux] Bash pacman 用法: 管理軟體包

## Overview
`pacman` 是一個用於 Arch Linux 及其衍生版的包管理工具。它可以用來安裝、更新和移除軟體包，並且能夠自動處理依賴關係。

## Usage
基本語法如下：
```bash
pacman [options] [arguments]
```

## Common Options
- `-S`：安裝或更新軟體包。
- `-R`：移除已安裝的軟體包。
- `-U`：從本地檔案安裝軟體包。
- `-Q`：查詢已安裝的軟體包。
- `-Sy`：更新軟體包資料庫。
- `-Syu`：更新所有已安裝的軟體包及其資料庫。

## Common Examples
- 安裝一個新的軟體包：
  ```bash
  pacman -S package_name
  ```

- 移除一個已安裝的軟體包：
  ```bash
  pacman -R package_name
  ```

- 更新所有已安裝的軟體包：
  ```bash
  pacman -Syu
  ```

- 查詢已安裝的軟體包：
  ```bash
  pacman -Q
  ```

- 從本地檔案安裝一個軟體包：
  ```bash
  pacman -U /path/to/package.pkg.tar.zst
  ```

## Tips
- 在執行更新命令之前，建議先備份重要資料，以防止意外情況發生。
- 使用 `pacman -Qdt` 可以查詢系統中未被其他軟體包依賴的孤立軟體包，這有助於清理不再需要的軟體。
- 定期更新系統以確保安全性和穩定性，使用 `pacman -Syu` 是一個好習慣。