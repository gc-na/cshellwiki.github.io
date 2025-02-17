# [Linux] Bash strace Uso: Trace system calls and signals

## Overview
The `strace` command is a powerful diagnostic tool in Linux that allows users to monitor the system calls and signals received by a process. It is commonly used for debugging and analyzing the behavior of programs, providing insights into what a program is doing at the system level.

## Usage
The basic syntax of the `strace` command is as follows:

```bash
strace [options] [arguments]
```

## Common Options
- `-c`: Count time, calls, and errors for each system call.
- `-e trace=<set>`: Specify which system calls to trace (e.g., `-e trace=open`).
- `-f`: Follow forks, tracing child processes as well.
- `-o <file>`: Output the trace to a specified file instead of standard error.
- `-p <pid>`: Attach to a running process with the given process ID.

## Common Examples

1. **Trace a command**:
   To trace the system calls made by the `ls` command:
   ```bash
   strace ls
   ```

2. **Trace specific system calls**:
   To trace only the `open` and `close` system calls made by a command:
   ```bash
   strace -e trace=open,close ls
   ```

3. **Output to a file**:
   To save the output of the trace to a file named `trace_output.txt`:
   ```bash
   strace -o trace_output.txt ls
   ```

4. **Count system calls**:
   To count the number of calls made by a command:
   ```bash
   strace -c ls
   ```

5. **Attach to a running process**:
   To attach to a process with PID 1234 and trace its system calls:
   ```bash
   strace -p 1234
   ```

## Tips
- Use `strace` with caution on production systems, as it can generate a lot of output and may impact performance.
- Combine `strace` with `grep` to filter specific system calls or messages for easier analysis:
  ```bash
  strace ls | grep open
  ```
- Familiarize yourself with common system calls to better understand the output from `strace`.