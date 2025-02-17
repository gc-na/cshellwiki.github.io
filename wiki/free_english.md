# [Linux] Bash free comando: mostrar información de memoria

## Overview
The `free` command in Linux is used to display information about the system's memory usage, including total, used, free, shared, buffer/cache, and available memory. This command is useful for monitoring memory usage and diagnosing performance issues.

## Usage
The basic syntax of the `free` command is as follows:

```bash
free [options] [arguments]
```

## Common Options
- `-h`: Display the memory sizes in a human-readable format (e.g., KB, MB, GB).
- `-m`: Show the memory usage in megabytes.
- `-g`: Show the memory usage in gigabytes.
- `-s <seconds>`: Continuously display memory usage at specified intervals (in seconds).
- `-t`: Display a total line that summarizes the memory usage.

## Common Examples

1. **Display memory usage in human-readable format:**
   ```bash
   free -h
   ```

2. **Show memory usage in megabytes:**
   ```bash
   free -m
   ```

3. **Show memory usage in gigabytes:**
   ```bash
   free -g
   ```

4. **Continuously display memory usage every 5 seconds:**
   ```bash
   free -s 5
   ```

5. **Display memory usage with a total line:**
   ```bash
   free -t -h
   ```

## Tips
- Use the `-h` option for easier readability when checking memory usage.
- Combine the `-s` option with `-h` for a continuous, easy-to-read output.
- Regularly monitor memory usage, especially on servers, to ensure optimal performance and prevent memory exhaustion.