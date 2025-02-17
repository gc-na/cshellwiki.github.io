# [Linux] Bash ulimit Uso: Control resource limits for user processes

## Overview
The `ulimit` command in Bash is used to control the resource limits for user processes. It allows users to set or display the limits on system resources available to the shell and its child processes, helping to prevent a single user from consuming all system resources.

## Usage
The basic syntax of the `ulimit` command is as follows:

```bash
ulimit [options] [arguments]
```

## Common Options
- `-a`: Displays all current limits.
- `-c [size]`: Sets the maximum size of core files created.
- `-d [size]`: Sets the maximum size of a process's data segment.
- `-f [size]`: Sets the maximum size of files that can be created.
- `-l [size]`: Sets the maximum size of locked-in-memory address space.
- `-m [size]`: Sets the maximum resident set size.
- `-n [number]`: Sets the maximum number of open file descriptors.
- `-s [size]`: Sets the maximum stack size.
- `-t [seconds]`: Sets the maximum amount of CPU time in seconds.

## Common Examples
Here are some practical examples of using `ulimit`:

1. **Display all current limits:**
   ```bash
   ulimit -a
   ```

2. **Set the maximum number of open files to 1024:**
   ```bash
   ulimit -n 1024
   ```

3. **Set the maximum size of core files to 0 (disable core dumps):**
   ```bash
   ulimit -c 0
   ```

4. **Set the maximum stack size to 8 MB:**
   ```bash
   ulimit -s 8192
   ```

5. **Check the maximum CPU time allowed for processes:**
   ```bash
   ulimit -t
   ```

## Tips
- Always check the current limits with `ulimit -a` before making changes to understand the existing configuration.
- Use caution when increasing limits, as it may affect system stability if a process consumes excessive resources.
- Changes made with `ulimit` are only effective for the current shell session and its child processes; for permanent changes, consider modifying system configuration files like `/etc/security/limits.conf`.