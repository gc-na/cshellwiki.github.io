# [Linux] Bash last command: Display login history

## Overview
The `last` command is used in Linux to display a list of the most recent logins to the system. It reads from the `/var/log/wtmp` file, which records all logins and logouts. This command is useful for monitoring user activity and understanding who accessed the system and when.

## Usage
The basic syntax of the `last` command is as follows:

```bash
last [options] [arguments]
```

## Common Options
- `-a`: Display the hostname on the last column.
- `-n <number>`: Limit the output to the last `<number>` of entries.
- `-R`: Suppress the display of the hostname.
- `-x`: Show system shutdown entries and run level changes.

## Common Examples
Here are some practical examples of using the `last` command:

1. **Display all login history:**
   ```bash
   last
   ```

2. **Show the last 5 logins:**
   ```bash
   last -n 5
   ```

3. **Display logins with hostnames:**
   ```bash
   last -a
   ```

4. **Suppress hostname display:**
   ```bash
   last -R
   ```

5. **Include system shutdown entries:**
   ```bash
   last -x
   ```

## Tips
- Use `last | less` to paginate through the output if there are many entries.
- Combine `last` with `grep` to filter results for a specific user, e.g., `last | grep username`.
- Remember that the `last` command shows historical data, so it may not reflect current user sessions. For current sessions, consider using the `who` command.