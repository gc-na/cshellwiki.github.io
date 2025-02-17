# [Linux] Bash watch uso: Monitor command output periodically

## Overview
The `watch` command in Bash is a utility that allows users to execute a specified command at regular intervals, displaying the output in the terminal. This is particularly useful for monitoring changes in command output, such as system resource usage or file modifications.

## Usage
The basic syntax of the `watch` command is as follows:

```bash
watch [options] [arguments]
```

## Common Options
- `-n <seconds>`: Specify the interval in seconds between command executions. The default is 2 seconds.
- `-d`: Highlight the differences between successive updates.
- `-t`: Turn off the header showing the command being run and the interval.
- `-x`: Allow the execution of commands that require a terminal.

## Common Examples
Here are some practical examples of using the `watch` command:

1. **Monitor Disk Usage**:
   ```bash
   watch df -h
   ```
   This command will display the disk usage of all mounted filesystems every 2 seconds.

2. **Check Running Processes**:
   ```bash
   watch -n 5 ps aux
   ```
   This command will execute `ps aux` every 5 seconds, showing the currently running processes.

3. **Monitor a Log File**:
   ```bash
   watch tail -n 10 /var/log/syslog
   ```
   This command will display the last 10 lines of the syslog file, updating every 2 seconds.

4. **Highlight Changes in a Directory**:
   ```bash
   watch -d ls -l
   ```
   This command will list the files in the current directory and highlight any changes in the output.

5. **Check System Load**:
   ```bash
   watch -n 1 uptime
   ```
   This command will show the system uptime and load averages every second.

## Tips
- Use the `-d` option to easily spot changes in the output, which can be particularly helpful when monitoring logs or resource usage.
- Adjust the interval with the `-n` option to suit your needs; shorter intervals can provide real-time updates, while longer intervals can reduce system load.
- Combine `watch` with other commands to create powerful monitoring tools, such as checking network connections or monitoring specific application logs.