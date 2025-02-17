# [Linux] Bash nice Usage: Adjust process priority

## Overview
The `nice` command in Bash is used to run a program with a modified scheduling priority. By default, processes run with a priority of 0, but you can use `nice` to increase or decrease this priority, which can help manage system resources effectively. Lowering the priority of a process allows other processes to run more smoothly, while increasing it can help ensure that a critical task gets the CPU time it needs.

## Usage
The basic syntax of the `nice` command is as follows:

```bash
nice [options] [command [arguments]]
```

## Common Options
- `-n, --adjustment=N`: Set the priority adjustment value, where N can be a positive or negative integer. The default is 10.
- `-h, --help`: Display help information about the command.
- `-v, --version`: Show version information for the `nice` command.

## Common Examples
Here are several practical examples of using the `nice` command:

1. **Run a command with default nice value (10):**
   ```bash
   nice myscript.sh
   ```

2. **Run a command with a specific nice value (e.g., -5):**
   ```bash
   nice -n -5 myscript.sh
   ```

3. **Run a command with increased priority (e.g., 19):**
   ```bash
   nice -n 19 myscript.sh
   ```

4. **Check the nice value of a running process:**
   ```bash
   ps -o pid,nice,cmd
   ```

5. **Start a CPU-intensive task with lower priority:**
   ```bash
   nice -n 19 ./heavy_task
   ```

## Tips
- Use `nice` for background tasks that are not time-sensitive to free up CPU resources for other processes.
- To check the nice value of a running process, use the `ps` command as shown in the examples.
- Remember that only the superuser can set a negative nice value (higher priority). Regular users can only increase the nice value (lower priority).