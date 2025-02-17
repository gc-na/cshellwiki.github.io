# [台灣] Bash rmdir 使用方法: 刪除空目錄

## Overview
`rmdir` 命令用於刪除空的目錄。如果目錄中有檔案或其他目錄，則無法使用此命令刪除。

## Usage
基本語法如下：
```
rmdir [選項] [參數]
```

## Common Options
- `-p`：同時刪除目錄及其父目錄（如果父目錄也為空）。
- `--ignore-fail-on-non-empty`：忽略非空目錄的錯誤，不會顯示錯誤訊息。

## Common Examples
1. 刪除一個空目錄：
   ```bash
   rmdir my_empty_directory
   ```

2. 同時刪除多個空目錄：
   ```bash
   rmdir dir1 dir2 dir3
   ```

3. 刪除一個空目錄及其父目錄：
   ```bash
   rmdir -p parent_directory/child_directory
   ```

4. 忽略非空目錄的錯誤：
   ```bash
   rmdir --ignore-fail-on-non-empty non_empty_directory
   ```

## Tips
- 在使用 `rmdir` 前，請確認目錄是空的，否則命令將失敗。
- 使用 `-p` 選項時，確保所有要刪除的目錄都為空，否則父目錄不會被刪除。
- 可以使用 `ls` 命令先檢查目錄內容，確保其為空。