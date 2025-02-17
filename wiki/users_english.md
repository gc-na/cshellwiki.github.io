# [Linux] Bash users équivalent : Manage user accounts and groups

## Overview
The `users` command in Bash is used to display the usernames of users currently logged into the system. It provides a simple way to see who is actively using the system at any given time.

## Usage
The basic syntax of the `users` command is as follows:

```bash
users [options]
```

## Common Options
While the `users` command does not have many options, here are a couple that may be useful:

- `-n`: Suppresses the output of duplicate usernames, showing each user only once.
- `-r`: Displays the usernames of users who are logged in but are not currently using the terminal.

## Common Examples

1. **Display currently logged-in users:**
   ```bash
   users
   ```

2. **Display unique usernames of logged-in users:**
   ```bash
   users -n
   ```

3. **Display users logged in without terminal activity:**
   ```bash
   users -r
   ```

## Tips
- Use the `users` command in conjunction with other commands like `who` or `w` for more detailed information about logged-in users.
- Consider using `users -n` in scripts where you want to avoid duplicate entries for users logged in multiple times.
- Remember that the output of the `users` command reflects the current state of logged-in users, so it may change frequently.