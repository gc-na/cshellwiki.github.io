# [Linux] Bash history Uso: View command history

## Overview
The `history` command in Bash is used to display the list of commands that have been executed in the current shell session. This feature is particularly useful for recalling previous commands without needing to retype them, making it easier to manage and navigate your command-line tasks.

## Usage
The basic syntax of the `history` command is as follows:

```bash
history [options] [arguments]
```

## Common Options
- `-c`: Clear the entire command history.
- `-d offset`: Delete the history entry at the specified offset.
- `n`: Display the last `n` commands from the history list.
- `!n`: Execute the command at the specified history number `n`.

## Common Examples
Here are some practical examples of using the `history` command:

1. **Display the entire command history:**
   ```bash
   history
   ```

2. **Display the last 10 commands:**
   ```bash
   history 10
   ```

3. **Execute a specific command from history (e.g., command number 5):**
   ```bash
   !5
   ```

4. **Clear the command history:**
   ```bash
   history -c
   ```

5. **Delete a specific entry from history (e.g., entry number 3):**
   ```bash
   history -d 3
   ```

## Tips
- Use the `Ctrl + R` shortcut to search through your command history interactively.
- To quickly repeat the last command, you can use `!!`.
- Consider using `history > filename.txt` to save your command history to a file for future reference.