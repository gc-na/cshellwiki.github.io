# [Linux] Bash nohup用法: 运行命令而不受挂起影响

## Overview
The `nohup` command in Bash is used to run another command immune to hangups, allowing it to continue executing even after the user has logged out or the terminal has been closed. This is particularly useful for long-running processes.

## Usage
The basic syntax of the `nohup` command is as follows:

```bash
nohup [options] [arguments]
```

## Common Options
- `&`: Runs the command in the background.
- `-h`: Displays help information about the command.
- `-p`: Specifies the process ID to be used with the command.

## Common Examples
Here are some practical examples of using `nohup`:

1. **Running a script in the background:**
   ```bash
   nohup ./my_script.sh &
   ```
   This command runs `my_script.sh` in the background, allowing you to log out without stopping the script.

2. **Running a command with output redirected to a file:**
   ```bash
   nohup python my_script.py > output.log &
   ```
   This command runs `my_script.py` and redirects its output to `output.log`.

3. **Running a long-running process:**
   ```bash
   nohup tar -czf backup.tar.gz /path/to/directory &
   ```
   This command creates a compressed backup of a directory, allowing it to continue even if you log out.

4. **Checking the output of a nohup command:**
   ```bash
   tail -f nohup.out
   ```
   This command allows you to monitor the output of the last `nohup` command in real-time.

## Tips
- Always redirect output to a file to avoid cluttering the terminal.
- Use `&` to run the command in the background, freeing up your terminal for other tasks.
- Check the `nohup.out` file for any output or errors if you forget to redirect output.
- Combine `nohup` with other commands like `cron` for scheduled tasks that need to run without interruption.