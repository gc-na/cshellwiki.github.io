# [Linux] Bash swapon 使用法: 啟用交換空間

## Overview
`swapon` 命令用於啟用交換空間（swap space），這是一種在系統記憶體不足時使用的虛擬記憶體。透過啟用交換空間，系統可以將不常用的數據從 RAM 移動到硬碟，從而釋放 RAM 以供其他應用程序使用。

## Usage
基本語法如下：
```
swapon [options] [arguments]
```

## Common Options
- `-a`: 啟用在 `/etc/fstab` 中列出的所有交換空間。
- `-e`: 顯示啟用交換空間的錯誤。
- `--show`: 顯示當前啟用的交換空間狀態。
- `-p`: 設定交換空間的優先權。

## Common Examples
1. 啟用所有在 `/etc/fstab` 中定義的交換空間：
   ```bash
   swapon -a
   ```

2. 啟用特定的交換檔案：
   ```bash
   swapon /swapfile
   ```

3. 顯示當前啟用的交換空間：
   ```bash
   swapon --show
   ```

4. 設定交換空間的優先權：
   ```bash
   swapon -p 10 /swapfile
   ```

## Tips
- 確保在啟用交換空間之前，交換檔案或分區已經正確創建並格式化。
- 使用 `swapon --show` 來檢查當前的交換空間使用情況，這有助於監控系統性能。
- 定期檢查和調整交換空間的大小，以確保系統運行流暢。