# [Linux] Bash sleep Usage: Pause for a specified duration

## Overview
The `sleep` command in Bash is used to pause the execution of a script or command for a specified amount of time. This can be useful in various scenarios, such as waiting for a process to complete or creating delays in automated scripts.

## Usage
The basic syntax of the `sleep` command is as follows:

```bash
sleep [options] [duration]
```

## Common Options
- `-h`, `--help`: Display help information about the command.
- `-V`, `--version`: Show the version of the `sleep` command.

## Common Examples
Here are some practical examples of how to use the `sleep` command:

1. **Pause for 5 seconds:**
   ```bash
   sleep 5
   ```

2. **Pause for 2 minutes:**
   ```bash
   sleep 2m
   ```

3. **Pause for 1 hour:**
   ```bash
   sleep 1h
   ```

4. **Combine sleep with other commands:**
   ```bash
   echo "Starting process..."
   sleep 3
   echo "Process started!"
   ```

5. **Use sleep in a loop:**
   ```bash
   for i in {1..5}; do
       echo "Iteration $i"
       sleep 2
   done
   ```

## Tips
- Use `sleep` to create delays between commands in scripts to avoid overwhelming resources.
- Combine `sleep` with conditional statements to wait for specific conditions before proceeding.
- Remember that durations can be specified in seconds (default), minutes (`m`), hours (`h`), or days (`d`). This flexibility allows for precise timing in your scripts.