# [台灣] Bash htop 使用方法: 監控系統資源

## Overview
htop 是一個互動式的進程查看器，能夠顯示系統的資源使用情況，包括 CPU、記憶體和進程等。與傳統的 top 命令相比，htop 提供了更友好的使用者介面和更多的功能。

## Usage
基本語法如下：
```
htop [選項] [參數]
```

## Common Options
- `-h` 或 `--help`：顯示幫助信息。
- `-s` 或 `--sort`：指定排序方式，例如 CPU 使用率或記憶體使用率。
- `-p` 或 `--pid`：只顯示指定的進程 ID。
- `-u` 或 `--user`：只顯示指定用戶的進程。

## Common Examples
- 啟動 htop：
  ```bash
  htop
  ```

- 以特定用戶過濾進程：
  ```bash
  htop -u username
  ```

- 以 CPU 使用率排序：
  ```bash
  htop -s PERCENT_CPU
  ```

- 顯示特定進程 ID：
  ```bash
  htop -p 1234
  ```

## Tips
- 使用方向鍵在進程列表中導航，按 `F9` 可以終止選中的進程。
- 按 `F2` 進入設置，您可以自定義顯示的列和排序方式。
- 定期檢查系統資源使用情況，以便及時發現性能瓶頸。