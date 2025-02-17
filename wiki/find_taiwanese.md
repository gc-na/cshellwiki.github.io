# [台灣] Bash find 使用法: 尋找檔案名稱

## Overview
`find` 命令用於在檔案系統中搜尋符合特定條件的檔案和目錄。它可以根據名稱、大小、修改時間等多種條件進行搜尋，並支援遞迴搜尋。

## Usage
基本語法如下：
```
find [選項] [參數]
```

## Common Options
- `-name <pattern>`: 根據檔案名稱模式搜尋。
- `-type <type>`: 指定檔案類型，例如 `f`（檔案）或 `d`（目錄）。
- `-size <n>`: 根據檔案大小搜尋，`n` 可以是數字加上單位（如 `k`、`M`、`G`）。
- `-mtime <n>`: 根據檔案最後修改時間搜尋，`n` 為天數。
- `-exec <command> {} \;`: 對找到的每個檔案執行指定的命令。

## Common Examples
- 根據檔案名稱搜尋：
  ```bash
  find /path/to/search -name "example.txt"
  ```

- 搜尋所有的目錄：
  ```bash
  find /path/to/search -type d
  ```

- 搜尋大於 1MB 的檔案：
  ```bash
  find /path/to/search -size +1M
  ```

- 搜尋最近 7 天內修改過的檔案：
  ```bash
  find /path/to/search -mtime -7
  ```

- 對找到的檔案執行命令（例如刪除）：
  ```bash
  find /path/to/search -name "*.tmp" -exec rm {} \;
  ```

## Tips
- 使用 `-iname` 來進行不區分大小寫的名稱搜尋。
- 結合 `-print` 選項可以顯示找到的檔案。
- 使用 `-maxdepth` 限制搜尋的目錄層級，避免搜尋過深。
- 在執行 `-exec` 命令前，先用 `-print` 確認找到的檔案，避免意外刪除。