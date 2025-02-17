# [Linux] Bash mpstat Uso equivalente: Monitor CPU usage statistics

## Overview
The `mpstat` command in Bash is used to report processor-related statistics, providing insights into CPU usage across multiple processors. It helps in monitoring system performance and identifying bottlenecks.

## Usage
The basic syntax of the `mpstat` command is as follows:

```bash
mpstat [options] [interval] [count]
```

## Common Options
- `-P ALL`: Display statistics for all processors.
- `-u`: Show CPU usage (default).
- `-h`: Display output in human-readable format.
- `-V`: Show version information.

## Common Examples

1. **Display CPU usage for all processors:**
   ```bash
   mpstat -P ALL
   ```

2. **Monitor CPU usage every 2 seconds for 5 times:**
   ```bash
   mpstat 2 5
   ```

3. **Show CPU usage with human-readable output:**
   ```bash
   mpstat -h
   ```

4. **Display only the user and system CPU usage:**
   ```bash
   mpstat -u
   ```

5. **Check the version of mpstat:**
   ```bash
   mpstat -V
   ```

## Tips
- Use `mpstat` in combination with other monitoring tools like `top` or `htop` for a comprehensive view of system performance.
- Regularly monitor CPU usage to identify trends and potential performance issues.
- Consider using the `-P` option to focus on specific processors if your system has multiple CPUs.