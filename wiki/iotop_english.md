# [Linux] Bash iotop Usage: Monitor Disk I/O by Processes

## Overview
The `iotop` command is a handy tool for monitoring disk input/output (I/O) usage by processes in real-time. It provides a dynamic view of which processes are consuming the most I/O resources on your system, helping you identify potential bottlenecks and performance issues.

## Usage
The basic syntax of the `iotop` command is as follows:

```bash
iotop [options] [arguments]
```

## Common Options
- `-o`, `--only`: Show only processes or threads actually doing I/O.
- `-b`, `--batch`: Run in batch mode, useful for logging output.
- `-d`, `--delay`: Set the delay between updates (in seconds).
- `-p`, `--pid`: Monitor specific process IDs.
- `-n`, `--iter`: Set the number of iterations before exiting.

## Common Examples
Here are some practical examples of using `iotop`:

1. **Basic Usage**: To start monitoring I/O in real-time, simply run:
   ```bash
   iotop
   ```

2. **Show Only Processes Doing I/O**: To filter the output to show only processes that are currently performing I/O:
   ```bash
   iotop -o
   ```

3. **Batch Mode for Logging**: To run `iotop` in batch mode and log the output every 2 seconds for 10 iterations:
   ```bash
   iotop -b -d 2 -n 10
   ```

4. **Monitor Specific Process**: To monitor a specific process with PID 1234:
   ```bash
   iotop -p 1234
   ```

5. **Change Update Interval**: To change the update interval to 1 second:
   ```bash
   iotop -d 1
   ```

## Tips
- Run `iotop` with superuser privileges (using `sudo`) to see all processes, as some may be restricted for normal users.
- Use the `-b` option when you want to log the output to a file for further analysis.
- Regularly monitor your system's I/O to catch any unexpected spikes that could indicate issues with specific applications or processes.