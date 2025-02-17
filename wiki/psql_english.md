# [Linux] Bash psql uso: Interact with PostgreSQL databases

## Overview
The `psql` command is a terminal-based front-end for interacting with PostgreSQL databases. It allows users to execute SQL commands, manage database objects, and perform administrative tasks directly from the command line.

## Usage
The basic syntax of the `psql` command is as follows:

```bash
psql [options] [arguments]
```

## Common Options
- `-h, --host=HOST`: Specifies the database server's hostname or IP address.
- `-p, --port=PORT`: Specifies the port number to connect to the database server.
- `-U, --username=USERNAME`: Specifies the username to connect to the database.
- `-d, --dbname=DBNAME`: Specifies the name of the database to connect to.
- `-W`: Prompts for the password before connecting to the database.
- `-c, --command=COMMAND`: Executes a single command and exits.

## Common Examples
1. **Connect to a database**:
   ```bash
   psql -U myuser -d mydatabase
   ```

2. **Execute a SQL command directly**:
   ```bash
   psql -U myuser -d mydatabase -c "SELECT * FROM mytable;"
   ```

3. **Connect to a remote database**:
   ```bash
   psql -h 192.168.1.100 -U myuser -d mydatabase
   ```

4. **List all databases**:
   ```bash
   psql -U myuser -c "\l"
   ```

5. **Export query results to a file**:
   ```bash
   psql -U myuser -d mydatabase -c "COPY (SELECT * FROM mytable) TO '/path/to/file.csv' WITH CSV HEADER;"
   ```

## Tips
- Always use the `-W` option if you want to ensure that your password is not stored in the command history.
- Utilize the `\?` command within `psql` to get a list of available commands and options while in the interactive shell.
- Consider using environment variables like `PGUSER`, `PGPASSWORD`, and `PGDATABASE` to simplify your command-line usage.
- For complex queries, it may be easier to write them in a `.sql` file and execute them using `psql -f filename.sql`.