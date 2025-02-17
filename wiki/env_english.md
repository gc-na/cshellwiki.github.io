# [Linux] Bash env Uso equivalente: Manage environment variables

## Overview
The `env` command in Bash is used to run a program in a modified environment or to print the current environment variables. It is particularly useful for setting or altering the environment variables temporarily for a command without affecting the global environment.

## Usage
The basic syntax of the `env` command is as follows:

```bash
env [options] [arguments]
```

## Common Options
- `-i`: Start with an empty environment, ignoring the current environment variables.
- `-u`: Remove a specified variable from the environment.
- `-0`: Use a null character as the delimiter for output (useful for handling filenames with spaces).

## Common Examples

1. **Print all environment variables:**
   ```bash
   env
   ```

2. **Run a command with a modified environment variable:**
   ```bash
   env VAR=value command
   ```
   This sets `VAR` to `value` only for the duration of `command`.

3. **Remove an environment variable for a command:**
   ```bash
   env -u VAR command
   ```
   This runs `command` without the environment variable `VAR`.

4. **Start a command with an empty environment:**
   ```bash
   env -i command
   ```
   This runs `command` without any inherited environment variables.

5. **Use null character as a delimiter:**
   ```bash
   env -0 | xargs -0 command
   ```
   This is useful for passing filenames with spaces to `command`.

## Tips
- Use `env` to ensure that scripts run with the correct environment variables, especially when running in different contexts.
- When testing scripts, consider using `env -i` to isolate the script from existing environment variables.
- Always check the current environment with `env` before modifying it to avoid unintended consequences.