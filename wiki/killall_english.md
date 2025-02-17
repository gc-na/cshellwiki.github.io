# [Linux] Bash killall Uso: Termina procesos por nombre

## Overview
The `killall` command in Bash is used to terminate processes by their name. This command allows users to stop multiple instances of a program at once, making it a powerful tool for process management.

## Usage
The basic syntax of the `killall` command is as follows:

```bash
killall [options] [arguments]
```

## Common Options
- `-u, --user <username>`: Kill processes owned by the specified user.
- `-q, --quiet`: Suppress error messages for non-existent processes.
- `-I, --ignore-case`: Ignore case distinctions when matching process names.
- `-e, --exact`: Match the process name exactly.
- `-s, --signal <signal>`: Specify the signal to send to the processes (default is TERM).

## Common Examples
Here are several practical examples of using the `killall` command:

1. **Terminate all instances of a program:**
   ```bash
   killall firefox
   ```

2. **Kill processes owned by a specific user:**
   ```bash
   killall -u username
   ```

3. **Send a specific signal to a process:**
   ```bash
   killall -s SIGKILL process_name
   ```

4. **Ignore case when terminating a process:**
   ```bash
   killall -I process_name
   ```

5. **Suppress error messages for non-existent processes:**
   ```bash
   killall -q process_name
   ```

## Tips
- Always double-check the process name to avoid accidentally terminating the wrong application.
- Use the `-q` option to keep your terminal output clean when you know some processes may not exist.
- Consider using `ps aux | grep process_name` to verify which processes are running before using `killall`.
- Be cautious with the `-u` option, especially on shared systems, as it can affect other users' processes.