# [Linux] Bash who Usage: Display logged-in users

## Overview
The `who` command in Bash is used to display a list of users who are currently logged into the system. It provides information such as the username, terminal line, login time, and originating IP address or hostname.

## Usage
The basic syntax of the `who` command is as follows:

```bash
who [options] [arguments]
```

## Common Options
- `-a`: Display all available information, including users logged in and their idle times.
- `-b`: Show the last system boot time.
- `-q`: Display only the usernames and the number of users logged in.
- `-H`: Print the column headers for the output.
- `--help`: Display help information about the command.

## Common Examples

1. **Basic Usage**: Display all logged-in users.
   ```bash
   who
   ```

2. **Show Detailed Information**: Display all available information about logged-in users.
   ```bash
   who -a
   ```

3. **Last Boot Time**: Show when the system was last booted.
   ```bash
   who -b
   ```

4. **Count of Logged-in Users**: Display only the usernames and the count of users logged in.
   ```bash
   who -q
   ```

5. **Including Headers**: Display logged-in users with column headers.
   ```bash
   who -H
   ```

## Tips
- Use `who -q` for a quick overview of how many users are logged in without additional details.
- Combine `who` with other commands like `grep` to filter results based on specific usernames or terminals.
- Regularly check who is logged in to monitor system usage, especially on multi-user systems.