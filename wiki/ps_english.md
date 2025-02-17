# [Linux] Bash ps Usage equivalent: Display process status

## Overview
The `ps` command in Bash is used to display information about the currently running processes on a system. It provides a snapshot of the processes and their statuses, which can be useful for monitoring system performance and managing processes.

## Usage
The basic syntax of the `ps` command is as follows:

```bash
ps [options] [arguments]
```

## Common Options
Here are some common options you can use with the `ps` command:

- `-e` or `-A`: Show all processes.
- `-f`: Display full-format listing, including additional details like UID and command line.
- `-u [user]`: Show processes for a specific user.
- `-p [pid]`: Show information for a specific process ID.
- `aux`: A combination of options to show all users' processes in a detailed format.

## Common Examples
Here are some practical examples of using the `ps` command:

1. **Show all processes:**
   ```bash
   ps -e
   ```

2. **Show processes for a specific user:**
   ```bash
   ps -u username
   ```

3. **Show detailed information about all processes:**
   ```bash
   ps aux
   ```

4. **Show a specific process by its PID:**
   ```bash
   ps -p 1234
   ```

5. **Show processes in a full-format listing:**
   ```bash
   ps -ef
   ```

## Tips
- Use `ps aux | grep [process_name]` to filter and find specific processes quickly.
- Combine `ps` with other commands like `sort` or `head` to organize or limit the output, e.g., `ps aux | sort -rk 3,3 | head -n 10` to show the top 10 processes by CPU usage.
- Familiarize yourself with the output columns (like PID, USER, %CPU, %MEM) to better understand the process status.