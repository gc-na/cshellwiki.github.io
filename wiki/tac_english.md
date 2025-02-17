# [Linux] Bash tac Usage: Reverse file content line by line

## Overview
The `tac` command in Bash is used to concatenate and display files in reverse order, line by line. It reads the input file(s) and outputs the lines starting from the last line to the first, making it useful for viewing logs or any text data in reverse.

## Usage
The basic syntax of the `tac` command is as follows:

```bash
tac [options] [arguments]
```

## Common Options
- `-b`, `--before`: Place the separator before the line instead of after.
- `-s`, `--separator=STRING`: Use STRING as the line separator instead of the default newline.
- `-r`, `--regex`: Treat the separator as a regular expression.

## Common Examples

1. **Reverse a single file:**
   To reverse the lines of a file named `example.txt`:
   ```bash
   tac example.txt
   ```

2. **Reverse multiple files:**
   To reverse the lines of multiple files, `file1.txt` and `file2.txt`:
   ```bash
   tac file1.txt file2.txt
   ```

3. **Using a custom separator:**
   To reverse a file while using a comma as a separator:
   ```bash
   tac -s ',' example.txt
   ```

4. **Reverse with a separator before the line:**
   To place a separator before each line while reversing:
   ```bash
   tac -b example.txt
   ```

5. **Using regex as a separator:**
   To reverse lines using a regex pattern as a separator:
   ```bash
   tac -r -s '[[:space:]]' example.txt
   ```

## Tips
- Use `tac` in combination with other commands like `grep` or `sort` to process data more effectively.
- When working with large files, consider using `tac` with `less` for easier navigation:
  ```bash
  tac example.txt | less
  ```
- Remember that `tac` does not modify the original files; it only outputs the reversed content to the terminal or to another file if redirected.