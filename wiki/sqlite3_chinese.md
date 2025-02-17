# [Linux] Bash sqlite3 使用方法: 交互式数据库管理工具

## 概述
sqlite3 是一个轻量级的关系数据库管理系统，允许用户通过命令行界面与 SQLite 数据库进行交互。它支持 SQL 查询、数据库创建、数据插入和更新等多种功能。

## 用法
sqlite3 的基本语法如下：

```bash
sqlite3 [options] [arguments]
```

## 常用选项
- `-help`：显示帮助信息。
- `-version`：显示 sqlite3 的版本信息。
- `-init <file>`：在启动时执行指定的 SQL 文件。
- `-batch`：以批处理模式运行，不显示提示符。
- `-cmd <command>`：在启动时执行指定的 SQL 命令。

## 常见示例
1. **创建一个新的数据库**
   ```bash
   sqlite3 mydatabase.db
   ```

2. **执行 SQL 文件**
   ```bash
   sqlite3 mydatabase.db < script.sql
   ```

3. **创建表并插入数据**
   ```bash
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Alice');"
   ```

4. **查询数据**
   ```bash
   sqlite3 mydatabase.db "SELECT * FROM users;"
   ```

5. **导出查询结果到 CSV 文件**
   ```bash
   sqlite3 -header -csv mydatabase.db "SELECT * FROM users;" > users.csv
   ```

## 提示
- 使用 `.exit` 或 `Ctrl+D` 退出 sqlite3 命令行界面。
- 在执行复杂的 SQL 查询时，可以使用 `.schema` 查看数据库的表结构。
- 定期备份数据库文件，以防数据丢失。