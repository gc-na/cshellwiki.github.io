# [Linux] Bash parted 用法: 磁碟分割管理工具

## Overview
`parted` 是一個用於管理磁碟分割的命令行工具。它可以創建、刪除、調整大小和檢查磁碟分割，並支援多種檔案系統格式。

## Usage
基本語法如下：
```bash
parted [options] [arguments]
```

## Common Options
- `-l`：列出所有磁碟及其分割資訊。
- `-s`：靜默模式，不顯示提示訊息。
- `mkpart`：創建新的分割。
- `rm`：刪除指定的分割。
- `resizepart`：調整指定分割的大小。

## Common Examples
1. 列出所有磁碟及其分割：
   ```bash
   parted -l
   ```

2. 創建一個新的分割：
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. 刪除指定的分割：
   ```bash
   parted /dev/sda rm 1
   ```

4. 調整分割大小：
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

## Tips
- 在執行 `parted` 命令之前，建議備份重要資料，以防止資料損失。
- 使用 `-s` 參數可以在腳本中運行 `parted` 而不會產生多餘的輸出。
- 確保在操作磁碟時，選擇正確的設備名稱，以避免意外刪除或更改錯誤的分割。