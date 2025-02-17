# [Linux] Bash top Usage: Monitor system processes in real-time

## Overview
The `top` command is a powerful utility in Linux that provides a real-time view of the system's resource usage, including CPU and memory consumption. It displays a dynamic list of processes currently running on the system, allowing users to monitor system performance and manage processes effectively.

## Usage
The basic syntax of the `top` command is as follows:

```bash
top [options]
```

## Common Options
Here are some common options you can use with the `top` command:

- `-d <seconds>`: Set the delay between updates (default is 3 seconds).
- `-n <number>`: Specify the number of iterations to display before exiting.
- `-u <username>`: Show processes for a specific user.
- `-p <pid>`: Monitor a specific process by its process ID (PID).
- `-b`: Run in batch mode, useful for logging output.

## Common Examples

1. **Basic Usage**: Launch `top` to see the current processes.
   ```bash
   top
   ```

2. **Change Update Interval**: Set the update interval to 5 seconds.
   ```bash
   top -d 5
   ```

3. **Limit Output to a User**: Show processes for a specific user, e.g., `john`.
   ```bash
   top -u john
   ```

4. **Monitor a Specific Process**: Track a process with PID 1234.
   ```bash
   top -p 1234
   ```

5. **Batch Mode for Logging**: Output the process list to a file every 10 seconds for 5 iterations.
   ```bash
   top -b -d 10 -n 5 > top_output.txt
   ```

## Tips
- Use the `h` key while in `top` to access help and see a list of interactive commands.
- Press `q` to exit `top` quickly.
- You can sort processes by CPU or memory usage by pressing the `P` or `M` keys, respectively, while `top` is running.
- Consider using `htop`, an enhanced version of `top`, for a more user-friendly interface with additional features.