# [Linux] Bash iostat Uso: Monitor system input/output device loading

## Overview
The `iostat` command is a useful tool in Linux that provides statistics on CPU and input/output (I/O) device usage. It helps system administrators monitor system performance and identify potential bottlenecks by displaying how much time the CPU spends on various tasks and how effectively the I/O devices are being utilized.

## Usage
The basic syntax of the `iostat` command is as follows:

```bash
iostat [options] [arguments]
```

## Common Options
- `-c`: Display CPU usage statistics.
- `-d`: Show I/O statistics for devices.
- `-x`: Provide extended statistics, including utilization and average wait time.
- `-m`: Display statistics in megabytes.
- `-t`: Include a timestamp in the output.
- `-p [device]`: Show statistics for a specific device or partition.

## Common Examples
Here are some practical examples of using the `iostat` command:

1. **Basic CPU and I/O Statistics**
   ```bash
   iostat
   ```

2. **Display CPU Usage Only**
   ```bash
   iostat -c
   ```

3. **Show Device Statistics with Extended Information**
   ```bash
   iostat -dx
   ```

4. **Display Statistics in Megabytes**
   ```bash
   iostat -m
   ```

5. **Monitor a Specific Device**
   ```bash
   iostat -p sda
   ```

6. **Include a Timestamp in the Output**
   ```bash
   iostat -t
   ```

## Tips
- Use `iostat` in combination with other monitoring tools like `vmstat` and `mpstat` for a comprehensive view of system performance.
- Regularly monitor I/O statistics to identify trends and potential issues before they affect system performance.
- Consider running `iostat` with a specified interval to continuously monitor system performance over time, for example:
  ```bash
  iostat 5
  ```
  This command will update the statistics every 5 seconds.