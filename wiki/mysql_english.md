# [Linux] Bash mysql uso: Interactuar con bases de datos MySQL

## Overview
The `mysql` command is a command-line tool used to interact with MySQL databases. It allows users to execute SQL queries, manage databases, and perform administrative tasks directly from the terminal.

## Usage
The basic syntax of the `mysql` command is as follows:

```bash
mysql [options] [arguments]
```

## Common Options
- `-u, --user=name`: Specify the username to connect to the MySQL server.
- `-p, --password[=name]`: Prompt for the password of the user. If `name` is omitted, it will ask for it interactively.
- `-h, --host=name`: Connect to a specific host instead of the default localhost.
- `-P, --port=#`: Specify the port number to connect to the MySQL server.
- `-D, --database=name`: Select a specific database to use after connecting.

## Common Examples
Here are some practical examples of using the `mysql` command:

1. **Connecting to MySQL with a username and password:**
   ```bash
   mysql -u username -p
   ```

2. **Connecting to a remote MySQL server:**
   ```bash
   mysql -h remote_host -u username -p
   ```

3. **Selecting a specific database upon connection:**
   ```bash
   mysql -u username -p -D database_name
   ```

4. **Executing a SQL file:**
   ```bash
   mysql -u username -p database_name < script.sql
   ```

5. **Showing all databases:**
   ```bash
   mysql -u username -p -e "SHOW DATABASES;"
   ```

## Tips
- Always use strong passwords for your MySQL user accounts to enhance security.
- Use the `-e` option to execute single SQL commands directly from the command line without entering the MySQL shell.
- To avoid entering your password interactively, you can store it in a `.my.cnf` file in your home directory with appropriate permissions.
- Regularly back up your databases to prevent data loss. Use the `mysqldump` command for this purpose.