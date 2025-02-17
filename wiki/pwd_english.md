# [Linux] Bash pwd Usage equivalent: Print working directory

## Overview
The `pwd` command in Bash stands for "print working directory." It is used to display the current directory you are in within the terminal. This command is particularly useful for navigating the file system and confirming your location before executing other commands.

## Usage
The basic syntax of the `pwd` command is as follows:

```
pwd [options]
```

## Common Options
- `-L`: Display the logical current working directory, resolving symbolic links.
- `-P`: Display the physical current working directory, without resolving symbolic links.

## Common Examples
Here are some practical examples of using the `pwd` command:

1. **Basic Usage**: Simply type `pwd` to display the current directory.
   ```bash
   pwd
   ```

2. **Using the Logical Option**: To show the logical path, use the `-L` option.
   ```bash
   pwd -L
   ```

3. **Using the Physical Option**: To show the physical path, use the `-P` option.
   ```bash
   pwd -P
   ```

## Tips
- Use `pwd` before running commands that depend on your current directory to avoid errors.
- Combine `pwd` with other commands using command substitution, such as `cd "$(pwd)/subdirectory"` to navigate to a subdirectory based on your current location.
- Remember that `pwd` is a built-in command in most shells, so it is always available without needing to install additional software.