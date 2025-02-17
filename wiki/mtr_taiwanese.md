# [台灣] Bash mtr 使用方法: 網路路徑追蹤工具

## Overview
mtr（My Traceroute）是一個結合了 traceroute 和 ping 功能的網路診斷工具。它可以幫助使用者追蹤資料包在網路中的路徑，並顯示每一跳的延遲和丟包情況。

## Usage
基本語法如下：
```
mtr [options] [arguments]
```

## Common Options
- `-r`：以報告模式運行，顯示一次性結果。
- `-c <count>`：指定發送的封包數量。
- `-i <interval>`：設置發送封包的間隔時間（秒）。
- `-p`：顯示每一跳的端口號。
- `-n`：不解析主機名稱，僅顯示 IP 地址。

## Common Examples
1. 基本使用，追蹤到 Google 的路徑：
   ```bash
   mtr google.com
   ```

2. 使用報告模式，顯示一次性結果：
   ```bash
   mtr -r google.com
   ```

3. 設定發送 10 個封包：
   ```bash
   mtr -c 10 google.com
   ```

4. 設定封包發送間隔為 1 秒：
   ```bash
   mtr -i 1 google.com
   ```

5. 不解析主機名稱，只顯示 IP 地址：
   ```bash
   mtr -n google.com
   ```

## Tips
- 當網路連線不穩定時，使用 mtr 可以幫助快速找出問題所在。
- 在進行長時間的測試時，考慮使用 `-c` 參數來限制封包數量，避免過多的資料干擾結果。
- 使用 `-p` 參數可以幫助你了解每一跳的端口情況，這對於進一步的網路診斷非常有用。