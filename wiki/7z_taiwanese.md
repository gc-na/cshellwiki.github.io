# [台灣] Bash 7z 使用法: 壓縮和解壓縮檔案

## Overview
7z 是一個強大的壓縮工具，能夠有效地壓縮和解壓縮各種檔案格式。它支持多種壓縮算法，並且通常用於創建和管理壓縮檔案，以節省儲存空間和提高傳輸效率。

## Usage
基本語法如下：
```
7z [options] [arguments]
```

## Common Options
- `a`: 添加檔案到壓縮檔案中。
- `x`: 解壓縮檔案。
- `l`: 列出壓縮檔案中的檔案。
- `d`: 刪除壓縮檔案中的檔案。
- `t`: 測試壓縮檔案的完整性。

## Common Examples
- 壓縮檔案：
  ```bash
  7z a archive.7z file1.txt file2.txt
  ```
  
- 解壓縮檔案：
  ```bash
  7z x archive.7z
  ```

- 列出壓縮檔案內容：
  ```bash
  7z l archive.7z
  ```

- 刪除壓縮檔案中的特定檔案：
  ```bash
  7z d archive.7z file1.txt
  ```

- 測試壓縮檔案的完整性：
  ```bash
  7z t archive.7z
  ```

## Tips
- 使用 `-p` 選項來設置密碼保護壓縮檔案，例如：`7z a -pMyPassword archive.7z file.txt`。
- 定期測試壓縮檔案的完整性，以確保檔案未損壞。
- 對於大型檔案，考慮使用分割壓縮功能，以便於傳輸和存儲。