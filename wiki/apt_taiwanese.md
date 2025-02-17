# [Linux] Bash apt 用法: 管理軟體包

## Overview
`apt` 是一個用於在 Debian 及其衍生版本（如 Ubuntu）中管理軟體包的命令行工具。它可以用來安裝、更新和移除軟體包，並且能夠自動處理依賴關係。

## Usage
基本語法如下：
```bash
apt [options] [arguments]
```

## Common Options
- `install`: 安裝指定的軟體包。
- `remove`: 移除指定的軟體包。
- `update`: 更新可用的軟體包列表。
- `upgrade`: 升級已安裝的所有軟體包。
- `search`: 搜尋可用的軟體包。

## Common Examples
- 更新軟體包列表：
  ```bash
  sudo apt update
  ```

- 安裝一個軟體包（例如 `curl`）：
  ```bash
  sudo apt install curl
  ```

- 升級所有已安裝的軟體包：
  ```bash
  sudo apt upgrade
  ```

- 移除一個軟體包（例如 `curl`）：
  ```bash
  sudo apt remove curl
  ```

- 搜尋可用的軟體包（例如 `git`）：
  ```bash
  apt search git
  ```

## Tips
- 使用 `sudo` 來獲得管理員權限，以便安裝或移除軟體包。
- 定期執行 `apt update` 和 `apt upgrade` 以保持系統的最新狀態。
- 在安裝新軟體包之前，使用 `apt search` 確認該包的可用性及其名稱。