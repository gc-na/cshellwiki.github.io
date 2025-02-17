# [台灣] Bash hostname 用法: 顯示或設定主機名稱

## Overview
`hostname` 命令用於顯示或設定系統的主機名稱。主機名稱是用來識別網路上的設備，通常在網路通信中扮演重要角色。

## Usage
基本語法如下：
```
hostname [options] [arguments]
```

## Common Options
- `-a`, `--alias`：顯示主機的別名。
- `-d`, `--domain`：顯示主機的網域名稱。
- `-f`, `--fqdn`：顯示完全合格的域名（FQDN）。
- `-i`, `--ip-address`：顯示主機的 IP 地址。
- `-s`, `--short`：顯示主機的短名稱。

## Common Examples
- 顯示當前主機名稱：
  ```bash
  hostname
  ```

- 顯示主機的完全合格域名：
  ```bash
  hostname -f
  ```

- 顯示主機的 IP 地址：
  ```bash
  hostname -i
  ```

- 設定新的主機名稱：
  ```bash
  sudo hostname new-hostname
  ```

- 顯示主機的網域名稱：
  ```bash
  hostname -d
  ```

## Tips
- 在更改主機名稱後，建議重新啟動系統以確保所有服務都能正確識別新的名稱。
- 使用 `hostnamectl` 命令可以更方便地管理主機名稱，特別是在使用 systemd 的系統上。
- 確保新的主機名稱符合網路規範，避免使用特殊字符。