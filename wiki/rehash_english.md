# [Linux] Bash rehash Uso equivalente: Refresh command hash table

The `rehash` command is used to refresh the command hash table in the Bash shell, ensuring that any newly installed executables are recognized.

## Overview
The `rehash` command updates the internal hash table of commands in the current shell session. This is particularly useful after installing new software or modifying the PATH, as it allows the shell to recognize new commands without needing to restart the session.

## Usage
The basic syntax of the `rehash` command is as follows:

```bash
rehash [options] [arguments]
```

## Common Options
- There are no specific options for the `rehash` command; it simply refreshes the command hash table.

## Common Examples
Here are some practical examples of using the `rehash` command:

1. **Basic Usage After Installing Software**
   After installing a new command-line tool, run `rehash` to ensure it's recognized:
   ```bash
   rehash
   ```

2. **Using rehash in a Script**
   If you have a script that installs new commands, you can include `rehash` to refresh the command table:
   ```bash
   #!/bin/bash
   sudo apt install my-new-tool
   rehash
   ```

3. **When Modifying the PATH**
   If you change the PATH variable to include a new directory, use `rehash` to update the hash table:
   ```bash
   export PATH=$PATH:/new/directory
   rehash
   ```

## Tips
- **Use After Installation**: Always run `rehash` after installing new command-line tools to avoid "command not found" errors.
- **Check Hash Table**: You can use the `hash` command to view the current hash table before and after running `rehash` to see the changes.
- **Avoid Unnecessary Calls**: If you haven't installed new commands or changed the PATH, there's no need to run `rehash` as it won't have any effect.