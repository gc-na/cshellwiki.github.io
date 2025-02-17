# [Linux] Bash sqlite3 Uso: Interactuar con bases de datos SQLite

## Overview
The `sqlite3` command is a command-line interface for interacting with SQLite databases. It allows users to create, modify, and query SQLite databases directly from the terminal, making it a powerful tool for database management and manipulation.

## Usage
The basic syntax of the `sqlite3` command is as follows:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: Displays help information about the command and its options.
- `-version`: Shows the version of SQLite being used.
- `-init <file>`: Executes SQL commands from the specified file upon startup.
- `-batch`: Runs in batch mode, which suppresses interactive prompts and outputs results in a more script-friendly format.

## Common Examples
Here are some practical examples of using the `sqlite3` command:

### Creating a New Database
To create a new SQLite database named `mydatabase.db`, use the following command:

```bash
sqlite3 mydatabase.db
```

### Creating a Table
Once inside the SQLite prompt, you can create a table with the following SQL command:

```sql
CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT, age INTEGER);
```

### Inserting Data
To insert data into the `users` table, you can run:

```sql
INSERT INTO users (name, age) VALUES ('Alice', 30);
INSERT INTO users (name, age) VALUES ('Bob', 25);
```

### Querying Data
To retrieve data from the `users` table, use:

```sql
SELECT * FROM users;
```

### Exporting Data to a CSV File
To export the data from the `users` table to a CSV file, you can use:

```bash
sqlite3 mydatabase.db -header -csv "SELECT * FROM users;" > users.csv
```

## Tips
- Always back up your database before performing destructive operations.
- Use the `.exit` command to exit the SQLite prompt cleanly.
- Familiarize yourself with SQL syntax, as `sqlite3` relies on it for database operations.
- Utilize the `-init` option to automate the execution of SQL scripts when starting `sqlite3`.