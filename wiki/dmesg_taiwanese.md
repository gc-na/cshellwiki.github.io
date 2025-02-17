# [Linux] Bash dmesg 用法： 查看內核環境信息

## Overview
`dmesg` 命令用於顯示內核環境信息，特別是系統啟動時的消息和設備驅動程序的日誌。這些信息對於診斷硬體問題和系統錯誤非常有用。

## Usage
基本語法如下：
```
dmesg [options] [arguments]
```

## Common Options
- `-C`：清除當前的環境信息緩衝區。
- `-c`：顯示並清除環境信息緩衝區。
- `-n level`：設置消息的優先級，僅顯示等級及以上的消息。
- `-T`：將時間戳轉換為可讀格式。
- `-f facility`：僅顯示來自指定設施的消息。

## Common Examples
- 查看所有內核消息：
  ```bash
  dmesg
  ```

- 查看並清除內核消息：
  ```bash
  dmesg -c
  ```

- 以可讀的時間格式顯示內核消息：
  ```bash
  dmesg -T
  ```

- 只顯示特定優先級的消息（例如，錯誤消息）：
  ```bash
  dmesg -n 1
  ```

- 查看特定設施的消息（例如，驅動程序）：
  ```bash
  dmesg -f driver
  ```

## Tips
- 定期檢查 `dmesg` 輸出可以幫助及早發現潛在的硬體問題。
- 使用 `dmesg -T` 可以更容易地理解時間戳，特別是在排查問題時。
- 如果你需要持久保存日誌，可以考慮將輸出重定向到文件：
  ```bash
  dmesg > dmesg_log.txt
  ```