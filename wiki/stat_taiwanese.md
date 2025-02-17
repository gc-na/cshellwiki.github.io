# [Linux] Bash stat 用法: 獲取檔案狀態資訊

## Overview
`stat` 命令用於顯示檔案或檔案系統的狀態資訊，包括檔案大小、修改時間、權限等詳細資料。

## Usage
基本語法如下：
```bash
stat [options] [arguments]
```

## Common Options
- `-c` : 自訂輸出格式。
- `-f` : 顯示檔案系統的狀態資訊。
- `--format` : 指定輸出格式，與 `-c` 相同。
- `-L` : 顯示符號連結所指向的檔案的狀態資訊。

## Common Examples
1. 顯示檔案的狀態資訊：
   ```bash
   stat filename.txt
   ```

2. 使用自訂格式顯示檔案大小和修改時間：
   ```bash
   stat -c "Size: %s bytes, Modified: %y" filename.txt
   ```

3. 顯示目錄的狀態資訊：
   ```bash
   stat /path/to/directory
   ```

4. 顯示符號連結的狀態資訊：
   ```bash
   stat -L symlink
   ```

5. 顯示檔案系統的狀態資訊：
   ```bash
   stat -f /
   ```

## Tips
- 使用 `-c` 選項可以自訂輸出格式，這對於腳本自動化非常有用。
- 當需要檢查多個檔案時，可以使用通配符，例如 `stat *.txt` 來顯示所有 `.txt` 檔案的狀態資訊。
- 結合 `grep` 可以過濾出特定的狀態資訊，例如：
  ```bash
  stat filename.txt | grep "Modify"
  ```