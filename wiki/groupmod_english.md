# [Linux] Bash groupmod Usage: Modify existing groups

## Overview
The `groupmod` command in Bash is used to modify existing user groups on a Linux system. It allows administrators to change the group name, group ID, or other attributes of a specified group.

## Usage
The basic syntax of the `groupmod` command is as follows:

```bash
groupmod [options] [arguments]
```

## Common Options
- `-n, --new-name NEW_GROUP`: Change the name of the group to `NEW_GROUP`.
- `-g, --gid GID`: Change the group ID to `GID`.
- `-h, --help`: Display help information about the command.
- `-o, --non-unique`: Allow the group ID to be non-unique (not recommended).

## Common Examples
Here are some practical examples of using the `groupmod` command:

1. **Change the name of a group:**
   ```bash
   groupmod -n newgroup oldgroup
   ```

2. **Change the group ID:**
   ```bash
   groupmod -g 105 newgroup
   ```

3. **Change both the group name and ID:**
   ```bash
   groupmod -n newgroup -g 106 oldgroup
   ```

4. **Display help information:**
   ```bash
   groupmod --help
   ```

## Tips
- Always ensure that no users are currently logged in to the group you are modifying to prevent any issues.
- Use the `getent group` command to verify the changes made to the group.
- Be cautious when changing group IDs, as it may affect file permissions and access for users associated with that group.