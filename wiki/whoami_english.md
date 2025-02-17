# [Linux] Bash whoami Uso equivalente: Display current user name

## Overview
The `whoami` command is a simple yet effective tool in Bash that displays the username of the current user who is logged into the terminal session. It is particularly useful for confirming your identity in multi-user environments or when running scripts.

## Usage
The basic syntax of the `whoami` command is as follows:

```bash
whoami [options] [arguments]
```

## Common Options
The `whoami` command has very few options, but here are the most common ones:

- `--help`: Displays help information about the command and its usage.
- `--version`: Shows the version of the `whoami` command.

## Common Examples

1. **Display Current User**
   To simply display the username of the current user, you can run:
   ```bash
   whoami
   ```

2. **Using with Other Commands**
   You can use `whoami` in combination with other commands. For example, to check the current user and list their home directory:
   ```bash
   echo "Current user: $(whoami) - Home directory: ~$(whoami)"
   ```

3. **Check User in a Script**
   If you are writing a script and want to ensure it runs under a specific user, you can include:
   ```bash
   if [ "$(whoami)" != "desired_user" ]; then
       echo "This script must be run as desired_user"
       exit 1
   fi
   ```

## Tips
- Use `whoami` when troubleshooting permission issues to confirm you are logged in as the correct user.
- Combine `whoami` with other commands to create informative output in scripts.
- Remember that `whoami` will only show the username of the user executing the command, not the username of any other users logged into the system.