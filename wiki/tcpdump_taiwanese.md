# [台灣] Bash tcpdump 使用方法: 捕獲和分析網路封包

## Overview
tcpdump 是一個強大的命令行工具，用於捕獲和分析網路封包。它可以幫助使用者監控網路流量，診斷網路問題，或進行安全分析。

## Usage
基本語法如下：
```bash
tcpdump [options] [arguments]
```

## Common Options
- `-i <interface>`: 指定要監控的網路介面。
- `-n`: 不解析主機名稱，直接顯示 IP 地址。
- `-v`: 顯示更詳細的封包資訊。
- `-c <count>`: 捕獲指定數量的封包後停止。
- `-w <file>`: 將捕獲的封包寫入檔案。
- `-r <file>`: 從檔案讀取封包進行分析。

## Common Examples
- 捕獲所有流量：
```bash
tcpdump
```

- 捕獲特定介面的流量：
```bash
tcpdump -i eth0
```

- 捕獲並保存前 100 個封包到檔案：
```bash
tcpdump -c 100 -w output.pcap
```

- 從檔案讀取並顯示封包：
```bash
tcpdump -r output.pcap
```

- 捕獲特定主機的流量：
```bash
tcpdump host 192.168.1.1
```

## Tips
- 使用 `-n` 選項可以加快捕獲速度，因為不需要解析主機名稱。
- 定期檢查捕獲的封包數量，以避免過多的資料導致系統性能下降。
- 將捕獲的封包寫入檔案後，可以使用 Wireshark 等工具進行更深入的分析。