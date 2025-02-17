# [Linux] Bash mysql 使用方法: 访问和管理MySQL数据库

## 概述
`mysql` 命令是一个用于与 MySQL 数据库进行交互的命令行工具。通过该命令，用户可以执行 SQL 查询、管理数据库、创建和修改表格等。

## 用法
基本的命令语法如下：
```bash
mysql [options] [arguments]
```

## 常用选项
- `-u`：指定用户名。
- `-p`：提示输入密码。
- `-h`：指定要连接的主机名。
- `-D`：指定要使用的数据库。
- `-e`：直接执行 SQL 语句。

## 常见示例
1. 连接到本地 MySQL 数据库：
   ```bash
   mysql -u root -p
   ```

2. 连接到远程 MySQL 数据库：
   ```bash
   mysql -u username -p -h remote_host
   ```

3. 选择特定数据库：
   ```bash
   mysql -u root -p -D database_name
   ```

4. 执行 SQL 查询：
   ```bash
   mysql -u root -p -e "SELECT * FROM table_name;"
   ```

5. 导入 SQL 文件：
   ```bash
   mysql -u root -p database_name < file.sql
   ```

## 提示
- 使用 `-p` 选项时，尽量不要在命令行中直接输入密码，以避免安全风险。
- 可以使用 `--help` 查看所有可用选项和详细信息。
- 定期备份数据库，以防数据丢失。