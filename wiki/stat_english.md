# [Linux] Bash stat Usage: Display file or file system status

## Overview
The `stat` command in Bash is used to display detailed information about a file or file system. This includes metadata such as file size, permissions, ownership, and timestamps for when the file was last accessed, modified, or changed.

## Usage
The basic syntax of the `stat` command is as follows:

```bash
stat [options] [arguments]
```

## Common Options
- `-c` or `--format`: Specify a custom output format.
- `-f` or `--file-system`: Display information about the file system instead of the file.
- `--help`: Show help information about the command and its options.
- `--version`: Display the version of the `stat` command.

## Common Examples
Here are some practical examples of using the `stat` command:

1. **Basic file information:**
   ```bash
   stat filename.txt
   ```

2. **Custom format output:**
   ```bash
   stat -c '%n: %s bytes' filename.txt
   ```

3. **File system information:**
   ```bash
   stat -f /
   ```

4. **Display version information:**
   ```bash
   stat --version
   ```

5. **Detailed information about multiple files:**
   ```bash
   stat file1.txt file2.txt
   ```

## Tips
- Use the `-c` option to customize the output to show only the information you need, which can be useful for scripting.
- When checking file systems, the `-f` option can provide insights into disk usage and available space.
- Always check the man page (`man stat`) for the most up-to-date options and usage examples specific to your system.