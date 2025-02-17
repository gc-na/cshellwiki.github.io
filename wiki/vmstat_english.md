# [Linux] Bash vmstat Uso equivalente: Monitor system performance

## Overview
The `vmstat` command is a tool used in Unix-like operating systems to report virtual memory statistics. It provides insights into system performance, including memory usage, processes, paging, block I/O, traps, and CPU activity. This information can help system administrators diagnose performance issues and optimize resource usage.

## Usage
The basic syntax of the `vmstat` command is as follows:

```bash
vmstat [options] [interval] [count]
```

- `options`: Various flags to modify the command's behavior.
- `interval`: The time in seconds between updates.
- `count`: The number of updates to display.

## Common Options
- `-a`: Show active and inactive memory.
- `-m`: Display memory statistics.
- `-s`: Provide a summary of memory statistics.
- `-d`: Show disk statistics.
- `-t`: Display the time in the output.

## Common Examples

1. **Basic Memory and CPU Statistics**
   ```bash
   vmstat
   ```
   This command displays a snapshot of memory and CPU usage.

2. **Continuous Monitoring Every 2 Seconds**
   ```bash
   vmstat 2
   ```
   This command updates the statistics every 2 seconds until interrupted.

3. **Display Statistics for 5 Intervals of 3 Seconds**
   ```bash
   vmstat 3 5
   ```
   This command shows the statistics every 3 seconds for a total of 5 updates.

4. **Show Active and Inactive Memory**
   ```bash
   vmstat -a
   ```
   This command provides details on active and inactive memory usage.

5. **Display Disk Statistics**
   ```bash
   vmstat -d
   ```
   This command shows statistics related to disk I/O.

## Tips
- Use `vmstat` in combination with other monitoring tools like `top` or `iostat` for a comprehensive view of system performance.
- Regularly monitor your system with `vmstat` to identify trends in resource usage over time.
- Pay attention to the `si` (swap in) and `so` (swap out) columns; high values may indicate memory pressure and potential performance issues.