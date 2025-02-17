# [Linux] Bash col Usage: Format text for terminal output

## Overview
The `col` command in Bash is used to filter reverse line feeds from a text stream, making it useful for formatting text output for terminal display. It helps in cleaning up text that has been formatted for printing, ensuring that it appears correctly on the screen.

## Usage
The basic syntax of the `col` command is as follows:

```bash
col [options] [arguments]
```

## Common Options
- `-b`: Suppress backspaces, treating them as ordinary characters.
- `-x`: Use tab stops every 8 characters instead of the default 8-character tab stops.
- `-f`: Filter out form feeds, which can be useful for cleaning up text.

## Common Examples

1. **Basic Usage**: To filter a text file and display it correctly in the terminal:
   ```bash
   col < input.txt
   ```

2. **Suppressing Backspaces**: To handle text that contains backspace characters:
   ```bash
   col -b < input_with_backspaces.txt
   ```

3. **Using Tab Stops**: To format text with custom tab stops:
   ```bash
   col -x < input_with_tabs.txt
   ```

4. **Filtering Form Feeds**: To remove form feeds from a document:
   ```bash
   col -f < input_with_formfeeds.txt
   ```

## Tips
- Use `col` in combination with other commands like `man` to format manual pages for better readability.
- Always check the output of `col` with a small sample of your text to ensure it formats as expected.
- Consider piping the output of `col` to other commands, such as `less`, for easier navigation of long text outputs.