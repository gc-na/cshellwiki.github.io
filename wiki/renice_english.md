# [Linux] Bash renice uso: Adjust process priority

## Overview
The `renice` command in Bash is used to change the priority of running processes. It allows users to modify the "niceness" value of a process, which affects its scheduling priority. A lower niceness value means higher priority, while a higher niceness value means lower priority.

## Usage
The basic syntax of the `renice` command is as follows:

```bash
renice [options] [arguments]
```

## Common Options
- `-n, --priority <number>`: Specify the new niceness value. The value can range from -20 (highest priority) to 19 (lowest priority).
- `-p, --pid <pid>`: Change the priority of a specific process by its process ID (PID).
- `-g, --pgroup <pgroup>`: Change the priority of all processes in a specific process group.
- `-u, --user <user>`: Change the priority of all processes owned by a specific user.

## Common Examples
Here are some practical examples of using the `renice` command:

1. **Change the priority of a specific process:**
   To change the niceness value of a process with PID 1234 to 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. **Increase the priority of a process:**
   To set the niceness value of a process with PID 5678 to -5:
   ```bash
   renice -n -5 -p 5678
   ```

3. **Change the priority for all processes of a user:**
   To change the niceness value of all processes owned by the user "john" to 15:
   ```bash
   renice -n 15 -u john
   ```

4. **Change the priority of a process group:**
   To change the priority of all processes in the group with ID 1000 to 0:
   ```bash
   renice -n 0 -g 1000
   ```

## Tips
- Use `renice` with caution, especially when lowering the niceness value, as it can affect system performance.
- You may need superuser privileges (using `sudo`) to change the priority of processes owned by other users.
- To check the current niceness value of a process, you can use the `ps` command with appropriate options.