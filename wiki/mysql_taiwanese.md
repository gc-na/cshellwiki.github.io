# [台灣] Bash mysql 用法: 管理MySQL資料庫

## Overview
`mysql` 是一個用於與 MySQL 資料庫進行互動的命令行工具。透過這個命令，使用者可以執行 SQL 查詢、管理資料庫、以及進行資料操作。

## Usage
基本語法如下：
```bash
mysql [options] [arguments]
```

## Common Options
- `-u`：指定使用者名稱。
- `-p`：提示輸入密碼。
- `-h`：指定主機名稱或 IP 地址。
- `-D`：指定要使用的資料庫名稱。
- `--execute`：直接執行指定的 SQL 查詢。

## Common Examples
1. 連接到本地 MySQL 伺服器：
   ```bash
   mysql -u root -p
   ```

2. 連接到指定主機的 MySQL 伺服器：
   ```bash
   mysql -h 192.168.1.100 -u username -p
   ```

3. 使用特定資料庫：
   ```bash
   mysql -u root -p -D my_database
   ```

4. 執行一條 SQL 查詢：
   ```bash
   mysql -u root -p --execute "SELECT * FROM my_table;"
   ```

5. 將查詢結果輸出到檔案：
   ```bash
   mysql -u root -p -D my_database -e "SELECT * FROM my_table;" > output.txt
   ```

## Tips
- 確保使用強密碼來保護資料庫安全。
- 使用 `--execute` 來快速執行單一查詢，避免進入互動模式。
- 定期備份資料庫，以防資料遺失。