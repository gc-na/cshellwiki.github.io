# [Linux] Bash tune2fs 使用法: 調整 ext2/ext3/ext4 檔案系統的參數

## Overview
`tune2fs` 是一個用於調整 ext2、ext3 和 ext4 檔案系統的工具。它可以用來修改檔案系統的參數，例如檔案系統的標籤、最大檔案數量、檔案系統檢查的頻率等。

## Usage
基本語法如下：
```bash
tune2fs [選項] [參數]
```

## Common Options
- `-L <label>`: 設定檔案系統的標籤。
- `-c <max-mount-count>`: 設定檔案系統的最大掛載次數。
- `-i <interval>`: 設定檔案系統檢查的時間間隔。
- `-O <feature>`: 啟用或禁用特定的檔案系統功能。
- `-e <error_behavior>`: 設定檔案系統遇到錯誤時的行為。

## Common Examples
以下是一些常見的使用範例：

1. 設定檔案系統標籤：
   ```bash
   tune2fs -L mylabel /dev/sda1
   ```

2. 設定最大掛載次數為 20 次：
   ```bash
   tune2fs -c 20 /dev/sda1
   ```

3. 設定檔案系統檢查的時間間隔為 30 天：
   ```bash
   tune2fs -i 30d /dev/sda1
   ```

4. 啟用大檔案支持：
   ```bash
   tune2fs -O bigalloc /dev/sda1
   ```

5. 設定遇到錯誤時的行為為報告：
   ```bash
   tune2fs -e remount-ro /dev/sda1
   ```

## Tips
- 在使用 `tune2fs` 前，建議先備份重要資料，以防不測。
- 使用 `-l` 選項可以查看檔案系統的當前參數設定：
  ```bash
  tune2fs -l /dev/sda1
  ```
- 確保在未掛載檔案系統或在單用戶模式下執行 `tune2fs`，以避免潛在的資料損壞。