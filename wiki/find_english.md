# [Linux] Bash find uso: find file names

## Overview
The `find` command is a powerful utility in Bash that allows users to search for files and directories within a specified location in the filesystem. It can search based on various criteria such as name, type, size, modification date, and more.

## Usage
The basic syntax of the `find` command is as follows:

```bash
find [options] [path] [expression]
```

- **options**: Modifiers that change the behavior of the command.
- **path**: The directory path where the search will start.
- **expression**: Criteria to filter the search results.

## Common Options
- `-name`: Search for files by name (case-sensitive).
- `-iname`: Search for files by name (case-insensitive).
- `-type`: Specify the type of file to search for (e.g., `f` for regular files, `d` for directories).
- `-size`: Search for files of a specific size (e.g., `+1M` for files larger than 1 MB).
- `-mtime`: Search for files modified within a certain number of days (e.g., `-mtime -7` for files modified in the last week).
- `-exec`: Execute a command on the files found (e.g., `-exec rm {} \;` to delete found files).

## Common Examples
Here are some practical examples of using the `find` command:

1. **Find files by name**:
   ```bash
   find /path/to/directory -name "filename.txt"
   ```

2. **Find files by name (case-insensitive)**:
   ```bash
   find /path/to/directory -iname "filename.txt"
   ```

3. **Find all directories**:
   ```bash
   find /path/to/directory -type d
   ```

4. **Find files larger than 10 MB**:
   ```bash
   find /path/to/directory -size +10M
   ```

5. **Find files modified in the last 30 days**:
   ```bash
   find /path/to/directory -mtime -30
   ```

6. **Delete all `.tmp` files**:
   ```bash
   find /path/to/directory -name "*.tmp" -exec rm {} \;
   ```

## Tips
- Always double-check your command, especially when using `-exec` to avoid accidental deletions.
- Use `-print` at the end of your command to display the results if you are using options that do not automatically print.
- Combine multiple criteria using logical operators like `-and` and `-or` for more complex searches.
- To test your `find` command without making changes, you can use `-print` to see what files would be affected.