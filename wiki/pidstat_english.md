# [Linux] Bash pidstat Uso: Monitor process statistics

## Overview
The `pidstat` command is a part of the `sysstat` package and is used to monitor individual process statistics in Linux. It provides detailed information about CPU usage, memory usage, and other performance metrics for running processes, making it a valuable tool for system administrators and developers.

## Usage
The basic syntax of the `pidstat` command is as follows:

```bash
pidstat [options] [arguments]
```

## Common Options
- `-h`: Display the help message with available options.
- `-p <pid>`: Monitor a specific process by its process ID (PID).
- `-r`: Report memory usage statistics.
- `-u`: Report CPU usage statistics.
- `-d`: Report I/O statistics.
- `-t`: Report statistics for threads.

## Common Examples

### Monitor CPU Usage of All Processes
To display CPU usage statistics for all running processes:

```bash
pidstat
```

### Monitor a Specific Process
To monitor a specific process with PID 1234:

```bash
pidstat -p 1234
```

### Monitor Memory Usage
To report memory usage statistics for all processes:

```bash
pidstat -r
```

### Monitor CPU and Memory Usage with Interval
To monitor CPU and memory usage every 2 seconds:

```bash
pidstat -r -u 2
```

### Monitor I/O Statistics
To report I/O statistics for all processes:

```bash
pidstat -d
```

## Tips
- Use the `-h` option to quickly view all available options and their descriptions.
- Combine options to get a comprehensive view of process performance, such as `pidstat -r -u -d`.
- Consider using `pidstat` in conjunction with other monitoring tools like `top` or `htop` for a more complete analysis of system performance.