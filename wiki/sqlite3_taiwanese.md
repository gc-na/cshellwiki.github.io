# [台灣] Bash sqlite3 使用法: 操作 SQLite 資料庫

## Overview
`sqlite3` 是一個命令列工具，用於與 SQLite 資料庫進行互動。它允許用戶執行 SQL 查詢、創建和管理資料庫以及執行各種資料操作。

## Usage
基本語法如下：
```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`：顯示幫助信息。
- `-version`：顯示 sqlite3 的版本。
- `-init <file>`：在啟動時執行指定的 SQL 檔案。
- `-batch`：以批處理模式運行，適合腳本使用。

## Common Examples
- **創建一個新的資料庫**
```bash
sqlite3 mydatabase.db
```

- **執行 SQL 查詢**
```bash
sqlite3 mydatabase.db "SELECT * FROM mytable;"
```

- **從檔案導入資料**
```bash
sqlite3 mydatabase.db ".import mydata.csv mytable"
```

- **導出資料到檔案**
```bash
sqlite3 mydatabase.db "SELECT * FROM mytable;" > output.txt
```

- **執行 SQL 檔案**
```bash
sqlite3 mydatabase.db < script.sql
```

## Tips
- 使用 `.tables` 命令可以快速查看資料庫中的所有表格。
- 在進行大量資料操作時，考慮使用 `BEGIN TRANSACTION` 和 `COMMIT` 來提高效能。
- 定期備份資料庫，以防止資料遺失。