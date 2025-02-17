# [台灣] Bash dstat 使用法: 監控系統資源

## Overview
dstat 是一個強大的系統監控工具，能夠即時顯示系統的資源使用情況，包括 CPU、記憶體、磁碟和網路等。它結合了多個監控工具的功能，提供了更全面的系統性能分析。

## Usage
基本語法如下：
```bash
dstat [options] [arguments]
```

## Common Options
- `-c`：顯示 CPU 使用情況。
- `-d`：顯示磁碟 I/O 使用情況。
- `-n`：顯示網路流量。
- `-m`：顯示記憶體使用情況。
- `-t`：顯示時間戳記。
- `--help`：顯示幫助信息。

## Common Examples
以下是一些常見的 dstat 使用範例：

1. 顯示 CPU 和記憶體使用情況：
   ```bash
   dstat -c -m
   ```

2. 顯示磁碟 I/O 和網路流量：
   ```bash
   dstat -d -n
   ```

3. 顯示所有可用的資源使用情況：
   ```bash
   dstat -cdmn
   ```

4. 每 2 秒更新一次顯示：
   ```bash
   dstat 2
   ```

## Tips
- 使用 `dstat --help` 來查看所有可用的選項和參數。
- 結合其他工具，如 `grep` 或 `awk`，可以過濾和分析 dstat 的輸出。
- 將 dstat 的輸出重定向到文件中，便於後續分析：
  ```bash
  dstat -cdmn > dstat_output.txt
  ```