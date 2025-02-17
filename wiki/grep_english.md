# [Linux] Bash grep Uso: Search text patterns in files

## Overview
The `grep` command is a powerful text search utility in Unix-like operating systems. It allows users to search for specific patterns within files or input data, making it an essential tool for text processing and data analysis.

## Usage
The basic syntax of the `grep` command is as follows:

```bash
grep [options] [arguments]
```

## Common Options
- `-i`: Ignore case distinctions in both the pattern and the input files.
- `-r`: Search recursively through directories.
- `-v`: Invert the match to select non-matching lines.
- `-n`: Show line numbers along with matching lines.
- `-l`: List the names of files with matching lines, without showing the lines themselves.
- `-c`: Count the number of matching lines.

## Common Examples
Here are several practical examples of using `grep`:

1. **Basic Search**: Search for the word "error" in a file named `logfile.txt`.
   ```bash
   grep "error" logfile.txt
   ```

2. **Case-Insensitive Search**: Search for "error" in a case-insensitive manner.
   ```bash
   grep -i "error" logfile.txt
   ```

3. **Recursive Search**: Search for "TODO" in all files within the current directory and its subdirectories.
   ```bash
   grep -r "TODO" .
   ```

4. **Show Line Numbers**: Display line numbers of matches when searching for "warning" in `file.txt`.
   ```bash
   grep -n "warning" file.txt
   ```

5. **Count Matches**: Count how many lines contain the word "success" in `results.txt`.
   ```bash
   grep -c "success" results.txt
   ```

6. **List Files with Matches**: List all files in the current directory that contain the word "config".
   ```bash
   grep -l "config" *
   ```

## Tips
- Use quotes around the search pattern to prevent shell interpretation of special characters.
- Combine `grep` with other commands using pipes to filter output, e.g., `dmesg | grep "usb"` to find USB-related messages.
- Regular expressions can be used for more complex pattern matching, enhancing the power of `grep`.