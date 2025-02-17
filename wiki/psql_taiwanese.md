# [Linux] Bash psql 使用法: 連接與操作 PostgreSQL 資料庫

## Overview
`psql` 是 PostgreSQL 的互動式命令列工具，允許使用者連接到 PostgreSQL 資料庫並執行 SQL 查詢。它提供了一個強大的環境來管理資料庫，執行查詢，並檢視資料。

## Usage
基本語法如下：
```bash
psql [options] [arguments]
```

## Common Options
- `-h`：指定資料庫伺服器的主機名稱。
- `-p`：指定連接的埠號，預設為 5432。
- `-U`：指定用戶名稱。
- `-d`：指定要連接的資料庫名稱。
- `-W`：要求輸入密碼。

## Common Examples
1. 連接到本地資料庫：
   ```bash
   psql -U username -d databasename
   ```

2. 連接到遠端資料庫：
   ```bash
   psql -h remote_host -U username -d databasename
   ```

3. 執行 SQL 檔案：
   ```bash
   psql -U username -d databasename -f filename.sql
   ```

4. 查詢資料表中的所有資料：
   ```bash
   psql -U username -d databasename -c "SELECT * FROM tablename;"
   ```

## Tips
- 使用 `\l` 命令可以列出所有資料庫。
- 使用 `\dt` 命令可以查看當前資料庫中的所有資料表。
- 若要退出 psql，請輸入 `\q`。
- 建議在執行重要操作前備份資料庫，以防資料損失。