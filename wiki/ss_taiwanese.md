# [Linux] Bash ss 使用法: 查看網路連線狀態

## Overview
`ss` 命令是一個用於顯示網路連線狀態的工具。它可以替代舊有的 `netstat` 命令，提供更快且更詳細的網路連接資訊，幫助用戶監控系統的網路活動。

## Usage
基本語法如下：
```bash
ss [選項] [參數]
```

## Common Options
- `-t`: 顯示 TCP 連接。
- `-u`: 顯示 UDP 連接。
- `-l`: 顯示正在監聽的 socket。
- `-p`: 顯示使用該 socket 的程序。
- `-n`: 以數字形式顯示地址和端口，避免解析主機名稱。

## Common Examples
- 查看所有 TCP 連接：
```bash
ss -t
```

- 查看所有 UDP 連接：
```bash
ss -u
```

- 查看所有正在監聽的 socket：
```bash
ss -l
```

- 查看所有連接及其對應的程序：
```bash
ss -t -p
```

- 以數字形式顯示所有 TCP 連接：
```bash
ss -tn
```

## Tips
- 使用 `ss` 時，搭配 `-p` 選項可以更容易地識別哪些程序正在使用網路資源。
- 結合 `grep` 命令可以過濾特定的連接，例如：
```bash
ss -t | grep 80
```
- 定期檢查網路連接狀態可以幫助及早發現潛在的網路問題。