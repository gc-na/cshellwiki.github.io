# [Linux] Bash usermod Uso: Modify user account attributes

## Overview
The `usermod` command in Bash is used to modify user account attributes on a Linux system. It allows system administrators to change various settings for existing user accounts, such as group memberships, home directories, and login shells.

## Usage
The basic syntax of the `usermod` command is as follows:

```bash
usermod [options] [username]
```

## Common Options
Here are some common options you can use with the `usermod` command:

- `-aG`: Append the user to the specified group(s).
- `-d`: Change the user's home directory.
- `-l`: Change the username.
- `-s`: Change the user's login shell.
- `-g`: Change the user's primary group.

## Common Examples

### 1. Add a user to a group
To add a user named `john` to the group `developers`, you would use:

```bash
usermod -aG developers john
```

### 2. Change the user's home directory
To change the home directory of the user `john` to `/home/john_new`, use:

```bash
usermod -d /home/john_new john
```

### 3. Change the username
To change the username from `john` to `johnny`, execute:

```bash
usermod -l johnny john
```

### 4. Change the user's login shell
To change the login shell of the user `john` to `/bin/bash`, run:

```bash
usermod -s /bin/bash john
```

### 5. Change the primary group
To change the primary group of the user `john` to `staff`, use:

```bash
usermod -g staff john
```

## Tips
- Always ensure you have the necessary permissions (usually root) to modify user accounts.
- Use the `-l` option with caution, as changing a username can affect file ownership and user permissions.
- After modifying a user’s group memberships, the user may need to log out and back in for changes to take effect.
- Consider backing up user data before making significant changes to user accounts.