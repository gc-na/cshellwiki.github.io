# [Linux] Bash stty Uso: Configure terminal line settings

## Overview
The `stty` command in Bash is used to change and print terminal line settings. It allows users to modify various attributes of the terminal interface, such as input and output settings, control characters, and more. This command is particularly useful for customizing the behavior of terminal sessions.

## Usage
The basic syntax of the `stty` command is as follows:

```bash
stty [options] [arguments]
```

## Common Options
Here are some common options you can use with `stty`:

- `-a`: Display all current settings.
- `-g`: Print the current settings in a form that can be reused.
- `erase`: Set the erase character.
- `kill`: Set the kill character.
- `intr`: Set the interrupt character.
- `sane`: Reset the terminal to reasonable settings.

## Common Examples
Here are some practical examples of using the `stty` command:

1. **Display current settings:**
   ```bash
   stty -a
   ```

2. **Set the erase character to backspace:**
   ```bash
   stty erase ^H
   ```

3. **Set the interrupt character to Ctrl+C:**
   ```bash
   stty intr ^C
   ```

4. **Reset the terminal to sane settings:**
   ```bash
   stty sane
   ```

5. **Save current settings to a variable:**
   ```bash
   settings=$(stty -g)
   ```

6. **Restore settings from a variable:**
   ```bash
   stty $settings
   ```

## Tips
- Always check your current settings with `stty -a` before making changes to avoid disrupting your terminal session.
- Use `stty sane` if you find your terminal behaving unexpectedly, as it restores default settings.
- Remember that changes made with `stty` are session-specific; they will not persist after closing the terminal.