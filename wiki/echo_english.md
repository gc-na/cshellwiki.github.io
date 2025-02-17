# [Linux] Bash echo用法: Displaying text to the terminal

## Overview
The `echo` command in Bash is used to display a line of text or a variable value to the terminal. It's a simple yet powerful tool for outputting information, making it essential for scripting and command-line operations.

## Usage
The basic syntax of the `echo` command is as follows:

```bash
echo [options] [arguments]
```

## Common Options
- `-n`: Suppresses the trailing newline, allowing the next output to appear on the same line.
- `-e`: Enables interpretation of backslash escapes (e.g., `\n` for newline, `\t` for tab).
- `-E`: Disables interpretation of backslash escapes (this is the default behavior).

## Common Examples

1. **Basic Text Output**
   ```bash
   echo "Hello, World!"
   ```

2. **Suppressing Newline**
   ```bash
   echo -n "This is on the same line."
   echo " And this continues."
   ```

3. **Using Backslash Escapes**
   ```bash
   echo -e "Line 1\nLine 2"
   ```

4. **Displaying Variable Values**
   ```bash
   name="Alice"
   echo "Hello, $name!"
   ```

5. **Combining Text and Variables**
   ```bash
   greeting="Good morning"
   echo "$greeting, $name!"
   ```

## Tips
- Use `echo -n` when you want to print multiple outputs on the same line.
- Remember to use quotes around strings that contain spaces to avoid unexpected behavior.
- For better readability, consider using `echo -e` to format your output with newlines and tabs when necessary.