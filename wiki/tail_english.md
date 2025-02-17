# [Linux] Bash tail Usage: Display the end of files

## Overview
The `tail` command in Bash is used to display the last part of files. It is particularly useful for monitoring log files or any file that is being updated in real-time, allowing users to see the most recent entries without opening the entire file.

## Usage
The basic syntax of the `tail` command is as follows:

```bash
tail [options] [arguments]
```

## Common Options
- `-n NUM`: Display the last NUM lines of the file. For example, `-n 10` shows the last 10 lines.
- `-f`: Follow the file as it grows. This is useful for monitoring log files in real-time.
- `-c NUM`: Display the last NUM bytes of the file.
- `--help`: Display help information about the command and its options.

## Common Examples
1. **Display the last 10 lines of a file:**
   ```bash
   tail filename.txt
   ```

2. **Display the last 20 lines of a file:**
   ```bash
   tail -n 20 filename.txt
   ```

3. **Follow a log file as it updates:**
   ```bash
   tail -f /var/log/syslog
   ```

4. **Display the last 50 bytes of a file:**
   ```bash
   tail -c 50 filename.txt
   ```

5. **Combine options to follow a file and show the last 5 lines:**
   ```bash
   tail -n 5 -f filename.txt
   ```

## Tips
- Use `tail -f` in combination with `Ctrl + C` to stop following the file when you're done.
- If you want to see more than just the last lines, consider using `head` in conjunction with `tail` to view specific sections of a file.
- You can use `tail` with pipes to filter output from other commands, enhancing its utility in scripts and command-line workflows.