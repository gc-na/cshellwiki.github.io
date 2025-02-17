# [Linux] Bash batch 使用法: 批次執行命令

## Overview
`batch` 命令用於在系統負載較低的時候執行一系列的命令。這個命令可以讓你安排在未來某個時間點執行的任務，通常是在系統的空閒時間進行。

## Usage
基本語法如下：
```
batch [options] [arguments]
```

## Common Options
- `-l`：顯示當前的系統負載。
- `-p`：指定執行的命令。
- `-h`：顯示幫助信息。

## Common Examples
以下是一些常見的使用範例：

1. **執行簡單命令**
   ```bash
   echo "echo Hello, World!" | batch
   ```

2. **執行多個命令**
   ```bash
   echo -e "date\nuptime" | batch
   ```

3. **使用選項顯示系統負載**
   ```bash
   batch -l
   ```

4. **指定特定命令執行**
   ```bash
   echo "python3 /path/to/script.py" | batch
   ```

## Tips
- 確保你有適當的權限來執行 `batch` 命令，否則可能會遇到權限問題。
- 使用 `atq` 命令來查看排程的任務。
- 定期檢查系統負載，以確保 `batch` 任務在適當的時間執行。