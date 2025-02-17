# [Linux] Bash modprobe 使用方法: 載入或卸載內核模組

## Overview
`modprobe` 是一個用於管理 Linux 內核模組的命令。它可以自動處理模組之間的依賴關係，並使得載入或卸載模組變得更加簡單。

## Usage
基本語法如下：
```
modprobe [選項] [模組名稱]
```

## Common Options
- `-r` 或 `--remove`: 卸載指定的模組。
- `-n` 或 `--dry-run`: 模擬執行，不實際載入或卸載模組。
- `-v` 或 `--verbose`: 顯示詳細的執行過程。
- `--show-depends`: 顯示模組的依賴關係。

## Common Examples
1. 載入一個模組，例如 `dummy`：
   ```bash
   modprobe dummy
   ```

2. 卸載一個模組，例如 `dummy`：
   ```bash
   modprobe -r dummy
   ```

3. 模擬載入一個模組，不實際執行：
   ```bash
   modprobe -n dummy
   ```

4. 顯示 `dummy` 模組的依賴關係：
   ```bash
   modprobe --show-depends dummy
   ```

5. 載入模組並顯示詳細信息：
   ```bash
   modprobe -v dummy
   ```

## Tips
- 在使用 `modprobe` 前，建議先使用 `lsmod` 查看當前已載入的模組，以避免重複載入。
- 使用 `modprobe -r` 時，請確保沒有其他模組依賴於要卸載的模組，否則卸載將失敗。
- 定期檢查系統的模組狀態，確保不必要的模組不會佔用系統資源。