# [Linux] Bash trap Usage: Handle signals and cleanup

## Overview
The `trap` command in Bash is used to specify commands that will be executed when the shell receives certain signals or when certain events occur. This is particularly useful for cleaning up resources or performing specific actions when a script is interrupted or terminated.

## Usage
The basic syntax of the `trap` command is as follows:

```bash
trap [commands] [signals]
```

- `[commands]`: The commands to execute when the specified signals are received.
- `[signals]`: The signals that will trigger the execution of the commands.

## Common Options
- `SIGINT`: Interrupt signal (usually sent when you press Ctrl+C).
- `SIGTERM`: Termination signal (default signal sent by the `kill` command).
- `EXIT`: Executes the specified commands when the script exits, regardless of the exit status.

## Common Examples

### Example 1: Cleanup on exit
This example demonstrates how to use `trap` to remove a temporary file when the script exits.

```bash
#!/bin/bash
temp_file="/tmp/my_temp_file.txt"
trap "rm -f $temp_file" EXIT

echo "Creating temporary file..."
touch $temp_file
echo "Temporary file created."
```

### Example 2: Handling SIGINT
In this example, the script will print a message and exit gracefully when interrupted.

```bash
#!/bin/bash
trap "echo 'Script interrupted!'; exit" SIGINT

while true; do
    echo "Running... (Press Ctrl+C to stop)"
    sleep 1
done
```

### Example 3: Multiple signals
You can specify multiple signals for the same command. Here’s how to handle both `SIGINT` and `SIGTERM`.

```bash
#!/bin/bash
trap "echo 'Terminating script...'; exit" SIGINT SIGTERM

while true; do
    echo "Working... (Press Ctrl+C or send SIGTERM to stop)"
    sleep 1
done
```

## Tips
- Always ensure that the commands specified in `trap` are simple and quick to execute to avoid delays in signal handling.
- Use `trap` for cleanup tasks such as removing temporary files or stopping background processes to maintain a clean environment.
- Remember to test your scripts to ensure that the `trap` commands behave as expected under various scenarios (e.g., normal exit, forced termination).