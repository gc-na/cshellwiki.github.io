# [Linux] Bash tail 使用法: 顯示檔案結尾的內容

## Overview
`tail` 命令用於顯示檔案的最後幾行內容，這在查看日誌檔案或監控檔案變更時特別有用。

## Usage
基本語法如下：
```
tail [options] [arguments]
```

## Common Options
- `-n [數量]`：顯示檔案的最後 [數量] 行，預設為 10 行。
- `-f`：持續追蹤檔案的新增內容，適合用於即時監控。
- `-c [數量]`：顯示檔案的最後 [數量] 字元。

## Common Examples
- 顯示最後 10 行檔案內容：
  ```bash
  tail filename.txt
  ```

- 顯示最後 20 行檔案內容：
  ```bash
  tail -n 20 filename.txt
  ```

- 持續追蹤日誌檔案的新增內容：
  ```bash
  tail -f /var/log/syslog
  ```

- 顯示最後 50 字元：
  ```bash
  tail -c 50 filename.txt
  ```

## Tips
- 使用 `tail -f` 來即時監控日誌檔案，這對於排錯非常有幫助。
- 結合 `grep` 使用可以過濾特定的關鍵字，例如：
  ```bash
  tail -f /var/log/syslog | grep "error"
  ```
- 若要查看多個檔案的尾部，可以將檔案名稱一起列出：
  ```bash
  tail file1.txt file2.txt
  ```