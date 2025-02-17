# [Linux] Bash mkswap 使用法: 創建交換空間

## Overview
`mkswap` 是一個用於設定交換空間的命令。交換空間是系統用來擴展虛擬記憶體的區域，當物理記憶體不足時，系統會將不常使用的資料移至交換空間。

## Usage
基本語法如下：
```
mkswap [選項] [參數]
```

## Common Options
- `-L, --label <label>`: 設定交換空間的標籤。
- `-f, --force`: 強制執行，即使檔案已經被標記為交換空間。
- `-p, --pagesize <size>`: 指定頁面大小。

## Common Examples
1. 創建一個交換檔案：
   ```bash
   sudo fallocate -l 1G /swapfile
   sudo mkswap /swapfile
   ```

2. 設定交換空間的標籤：
   ```bash
   sudo mkswap -L my_swap /swapfile
   ```

3. 強制重新設置已存在的交換空間：
   ```bash
   sudo mkswap -f /swapfile
   ```

## Tips
- 在創建交換檔案之前，確保檔案系統有足夠的空間。
- 使用 `swapon` 命令啟用交換空間，並使用 `swapoff` 停用。
- 定期檢查交換空間的使用情況，以確保系統性能。