# [Linux] Bash w Usage: Show who is logged on and what they are doing

## Overview
The `w` command in Bash is used to display information about the users currently logged into the system and their activities. It provides a snapshot of user sessions, including their login time, idle time, and the command they are currently executing.

## Usage
The basic syntax of the `w` command is as follows:

```bash
w [options] [arguments]
```

## Common Options
- `-h`: Suppresses the header line.
- `-s`: Displays the output in a short format, omitting the idle time and other details.
- `-u`: Shows the user’s idle time in a more human-readable format.
- `-f`: Displays the full hostname of the users instead of just the username.

## Common Examples
Here are some practical examples of using the `w` command:

1. **Basic Usage**
   ```bash
   w
   ```
   This command displays a list of users currently logged in along with their activities.

2. **Suppress Header**
   ```bash
   w -h
   ```
   This command shows the same information but without the header line.

3. **Short Format**
   ```bash
   w -s
   ```
   This command provides a concise output, omitting idle time and other details.

4. **Full Hostname**
   ```bash
   w -f
   ```
   This command displays the full hostname of the users logged in.

5. **Detailed User Activity**
   ```bash
   w -u
   ```
   This command shows user idle time in a more readable format.

## Tips
- Use `w` in combination with other commands like `grep` to filter specific users or activities.
- Regularly check the output of `w` to monitor system usage and identify any potential issues with user sessions.
- Consider using `w` alongside commands like `who` or `last` for a more comprehensive view of user activity on the system.