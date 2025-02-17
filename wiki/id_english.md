# [Linux] Bash id uso equivalente: Display user and group information

## Overview
The `id` command in Bash is used to display the user and group information for the current user or a specified user. It provides details such as user ID (UID), group ID (GID), and the groups the user belongs to.

## Usage
The basic syntax of the `id` command is as follows:

```bash
id [options] [username]
```

## Common Options
- `-u`: Display only the effective user ID.
- `-g`: Display only the effective group ID.
- `-G`: Display all group IDs the user belongs to.
- `-n`: Display names instead of numeric IDs.
- `-r`: Display the real ID instead of the effective ID.

## Common Examples

1. **Display information for the current user:**
   ```bash
   id
   ```

2. **Display information for a specific user:**
   ```bash
   id username
   ```

3. **Show only the effective user ID:**
   ```bash
   id -u
   ```

4. **Show only the effective group ID:**
   ```bash
   id -g
   ```

5. **List all group IDs for the current user:**
   ```bash
   id -G
   ```

6. **Display user information with names instead of numeric IDs:**
   ```bash
   id -n
   ```

## Tips
- Use `id` without any options to quickly check your current user and group information.
- Combine options for more detailed output, such as `id -Gn` to get group names.
- Remember that you can specify any username to check the information for other users, provided you have the necessary permissions.