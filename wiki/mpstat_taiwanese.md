# [台灣] Bash mpstat 使用法: 監控 CPU 使用率

## Overview
`mpstat` 是一個用於顯示各個 CPU 核心的使用情況的命令。它能夠提供每個 CPU 的使用率、空閒時間和其他性能指標，幫助使用者監控系統的性能。

## Usage
基本語法如下：
```
mpstat [options] [arguments]
```

## Common Options
- `-P ALL`：顯示所有 CPU 的統計資訊。
- `-u`：顯示 CPU 使用率，包括用戶、系統和空閒時間。
- `-h`：以可讀性更高的格式顯示數據。
- `-n`：顯示網路統計資訊。

## Common Examples
以下是一些常見的 `mpstat` 使用範例：

1. 顯示所有 CPU 的使用率：
   ```bash
   mpstat -P ALL
   ```

2. 每 1 秒更新一次 CPU 使用率：
   ```bash
   mpstat 1
   ```

3. 顯示 CPU 使用率並以可讀性更高的格式輸出：
   ```bash
   mpstat -u -h
   ```

4. 顯示特定 CPU 的使用率（例如 CPU 0）：
   ```bash
   mpstat -P 0
   ```

## Tips
- 定期使用 `mpstat` 來監控系統性能，特別是在高負載的情況下。
- 結合其他性能監控工具（如 `top` 或 `htop`）使用，可以獲得更全面的系統狀態。
- 使用 `mpstat` 的 `-n` 選項來檢查網路性能，這對於網路密集型應用特別有用。