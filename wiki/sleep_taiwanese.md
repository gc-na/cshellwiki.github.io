# [Linux] Bash sleep 用法: 暫停執行

## Overview
`sleep` 命令用於使腳本或命令暫停執行一段指定的時間。這在需要延遲操作或控制執行速度時非常有用。

## Usage
基本語法如下：
```
sleep [options] [arguments]
```

## Common Options
- `-s` : 以秒為單位指定暫停時間（預設單位）。
- `-m` : 以分鐘為單位指定暫停時間。
- `-h` : 以小時為單位指定暫停時間。
- `-d` : 以天為單位指定暫停時間。

## Common Examples
- 暫停 5 秒：
  ```bash
  sleep 5
  ```

- 暫停 2 分鐘：
  ```bash
  sleep 2m
  ```

- 暫停 1 小時：
  ```bash
  sleep 1h
  ```

- 暫停 3 天：
  ```bash
  sleep 3d
  ```

- 在腳本中使用 sleep 來控制命令執行的間隔：
  ```bash
  echo "開始..."
  sleep 3
  echo "3 秒後執行的命令"
  ```

## Tips
- 使用 `sleep` 可以幫助避免過快執行命令，特別是在處理需要時間的操作時。
- 在循環中搭配 `sleep` 使用，可以有效控制執行頻率，例如：
  ```bash
  while true; do
      echo "每 10 秒執行一次"
      sleep 10
  done
  ```
- 注意使用適當的時間單位，避免不必要的長時間等待。