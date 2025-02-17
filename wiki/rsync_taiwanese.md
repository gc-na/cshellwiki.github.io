# [台灣] Bash rsync 使用方法: 用於檔案同步和備份

## Overview
`rsync` 是一個強大的工具，用於在本地和遠端系統之間高效地同步和備份檔案。它可以僅傳輸變更的部分，從而節省帶寬和時間。

## Usage
基本語法如下：
```bash
rsync [options] [source] [destination]
```

## Common Options
- `-a`: 以檔案歸檔模式運行，保留檔案的所有屬性。
- `-v`: 顯示詳細的運行過程。
- `-z`: 在傳輸過程中壓縮檔案，以節省帶寬。
- `-r`: 遞迴地傳輸目錄。
- `--delete`: 在目標中刪除源中不存在的檔案。

## Common Examples
1. **基本檔案同步**
   ```bash
   rsync -av source/ destination/
   ```

2. **壓縮傳輸**
   ```bash
   rsync -avz source/ user@remote:/path/to/destination/
   ```

3. **遞迴同步整個目錄**
   ```bash
   rsync -ar source_directory/ destination_directory/
   ```

4. **刪除目標中不存在的檔案**
   ```bash
   rsync -av --delete source/ destination/
   ```

5. **同步到遠端伺服器**
   ```bash
   rsync -avz /local/path user@remote:/remote/path
   ```

## Tips
- 使用 `-n` 或 `--dry-run` 來模擬執行，檢查將要進行的變更，而不實際執行。
- 定期備份重要檔案，並考慮使用 `--delete` 選項來保持目標目錄的整潔。
- 結合 `cron` 任務自動化定期備份。