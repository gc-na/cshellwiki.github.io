# [Linux] Bash kill Usage: Terminate processes

## Overview
The `kill` command in Bash is used to send signals to processes, primarily to terminate them. It allows users to control running processes by specifying their process ID (PID) and the type of signal they wish to send.

## Usage
The basic syntax of the `kill` command is as follows:

```bash
kill [options] [arguments]
```

## Common Options
- `-l`: Lists all signal names.
- `-s SIGNAL`: Specifies the signal to send (default is TERM).
- `-n NUMBER`: Sends the signal corresponding to the specified number.
- `-p`: Suppresses the output of the command, useful for scripting.

## Common Examples
1. **Terminate a process by PID**:
   To terminate a process with PID 1234:
   ```bash
   kill 1234
   ```

2. **Send a specific signal**:
   To send the SIGKILL signal to a process with PID 5678:
   ```bash
   kill -s KILL 5678
   ```

3. **List all available signals**:
   To display all signal names:
   ```bash
   kill -l
   ```

4. **Terminate multiple processes**:
   To terminate processes with PIDs 2345 and 6789:
   ```bash
   kill 2345 6789
   ```

5. **Using signal numbers**:
   To send the signal number 9 (SIGKILL) to a process with PID 1234:
   ```bash
   kill -n 9 1234
   ```

## Tips
- Always try to use the default TERM signal before resorting to KILL, as it allows processes to clean up.
- Use `ps` or `top` commands to find the PID of the process you want to terminate.
- Be cautious when terminating processes, especially system processes, as it may lead to instability.