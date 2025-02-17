# [Linux] Bash ps 使用法: 顯示目前執行中的程序

## Overview
`ps` 命令用於顯示目前系統中正在執行的程序。它提供了有關每個程序的詳細資訊，例如進程ID、使用的CPU和記憶體等，對於系統管理和故障排除非常有用。

## Usage
基本語法如下：
```
ps [options] [arguments]
```

## Common Options
- `-e` 或 `-A`：顯示所有進程。
- `-f`：顯示完整格式，包括父進程ID等詳細資訊。
- `-u [user]`：顯示指定用戶的進程。
- `-aux`：顯示所有用戶的進程，並以詳細格式顯示。
- `--sort`：根據指定的欄位排序進程。

## Common Examples
- 顯示所有進程：
  ```bash
  ps -e
  ```

- 顯示當前用戶的進程：
  ```bash
  ps -u $USER
  ```

- 顯示所有進程並以詳細格式顯示：
  ```bash
  ps aux
  ```

- 顯示進程並根據記憶體使用量排序：
  ```bash
  ps aux --sort=-%mem
  ```

- 顯示進程樹：
  ```bash
  ps -ejH
  ```

## Tips
- 使用 `ps aux` 可以獲得最全面的進程資訊，適合進行系統監控。
- 結合 `grep` 命令可以快速查找特定進程，例如：
  ```bash
  ps aux | grep firefox
  ```
- 定期檢查進程可以幫助識別不必要的資源消耗，及時進行優化。