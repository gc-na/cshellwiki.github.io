# [Linux] Bash trap 用法: 捕捉信號

## Overview
`trap` 命令用來捕捉和處理信號，讓使用者能夠在接收到特定信號時執行自定義的命令或清理操作。這在編寫腳本時特別有用，因為它可以幫助管理腳本的終止和錯誤處理。

## Usage
基本語法如下：
```bash
trap [options] [commands] [signals]
```

## Common Options
- `-l`：列出所有可用的信號名稱。
- `-p`：顯示當前的 trap 設定。
- `commands`：當接收到指定的信號時要執行的命令。
- `signals`：要捕捉的信號名稱或數字。

## Common Examples
以下是一些常見的 `trap` 使用範例：

### 1. 捕捉退出信號
在腳本中捕捉 `EXIT` 信號，以便在腳本結束時執行清理操作：
```bash
trap 'echo "Script is exiting..."' EXIT
```

### 2. 捕捉中斷信號
捕捉 `SIGINT` 信號（通常是 Ctrl+C）：
```bash
trap 'echo "Caught SIGINT, cleaning up..."; exit' SIGINT
```

### 3. 捕捉多個信號
可以同時捕捉多個信號，並執行相同的命令：
```bash
trap 'echo "Caught SIGTERM or SIGINT"; exit' SIGTERM SIGINT
```

### 4. 清理臨時檔案
在腳本中使用 `trap` 來確保即使在錯誤情況下也能刪除臨時檔案：
```bash
tempfile=$(mktemp)
trap 'rm -f "$tempfile"; echo "Temporary file removed."' EXIT
```

## Tips
- 確保在腳本的開始部分設置 `trap`，這樣可以捕捉到所有相關的信號。
- 使用 `trap -` 可以清除先前設置的 trap。
- 測試你的 trap 設定，確保在不同情況下都能正常運作，特別是在錯誤或中斷的情況下。