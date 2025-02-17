# [Linux] Bash logout Usage: Exit the current shell session

## Overview
The `logout` command is used in Bash to terminate a login shell session. When executed, it logs the user out of the current session, effectively closing the terminal window or returning to the previous shell if nested.

## Usage
The basic syntax of the `logout` command is as follows:

```bash
logout [options]
```

## Common Options
The `logout` command does not have many options, but here are a few relevant points:

- **No options**: Simply typing `logout` will log you out of the current session.
  
Note: The `logout` command is typically only effective in login shells. If used in a non-login shell, it may result in an error.

## Common Examples

### Example 1: Basic Logout
To log out of your current shell session, simply type:

```bash
logout
```

### Example 2: Using in a Script
If you have a script running in a login shell and want to log out at the end, you can include:

```bash
# Your script commands
echo "Logging out..."
logout
```

### Example 3: Handling Errors
If you attempt to use `logout` in a non-login shell, you might see an error message. For example:

```bash
bash
logout
# Output: logout: not login shell
```

## Tips
- Always ensure you save your work before executing `logout`, as it will close your session and any unsaved changes will be lost.
- If you are using multiple terminal tabs or windows, be aware that `logout` will only affect the current session.
- For non-login shells, consider using `exit` instead, which will also terminate the shell session.