# [Linux] Bash ss Usage equivalent in English: Display socket statistics

## Overview
The `ss` command is a utility in Linux used to investigate sockets. It provides detailed information about network connections, including TCP, UDP, and UNIX domain sockets. `ss` is often preferred over the older `netstat` command due to its speed and the depth of information it can provide.

## Usage
The basic syntax of the `ss` command is as follows:

```bash
ss [options] [arguments]
```

## Common Options
- `-t`: Display TCP sockets.
- `-u`: Display UDP sockets.
- `-l`: Show listening sockets.
- `-p`: Show the process using the socket.
- `-n`: Show numerical addresses instead of resolving hostnames.
- `-a`: Show all sockets (listening and non-listening).
- `-s`: Display summary statistics.

## Common Examples

1. **Display all TCP sockets:**
   ```bash
   ss -t
   ```

2. **Show all listening sockets:**
   ```bash
   ss -l
   ```

3. **Display all UDP sockets:**
   ```bash
   ss -u
   ```

4. **Show all sockets with process information:**
   ```bash
   ss -p
   ```

5. **Display all sockets in numerical format:**
   ```bash
   ss -n
   ```

6. **Get a summary of socket statistics:**
   ```bash
   ss -s
   ```

## Tips
- Use `ss -tuln` to quickly view all listening TCP and UDP sockets with numerical addresses.
- Combine options for more specific queries, such as `ss -tunlp` to see all TCP and UDP sockets with process information.
- If you need to monitor socket activity in real-time, consider using `watch ss -tuln` to refresh the output periodically.