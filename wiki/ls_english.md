# [Linux] Bash ls Uso equivalente: Listar archivos y directorios

## Overview
The `ls` command is a fundamental utility in Unix-like operating systems that is used to list the contents of a directory. By default, it displays the names of files and directories within the current working directory.

## Usage
The basic syntax of the `ls` command is as follows:

```bash
ls [options] [arguments]
```

## Common Options
Here are some commonly used options with the `ls` command:

- `-l`: Displays detailed information about each file, including permissions, owner, size, and modification date.
- `-a`: Shows all files, including hidden files (those starting with a dot).
- `-h`: When used with `-l`, it makes file sizes human-readable (e.g., KB, MB).
- `-R`: Lists directories and their contents recursively.
- `-t`: Sorts files by modification time, showing the most recently modified files first.
- `-S`: Sorts files by size, with the largest files first.

## Common Examples

Here are some practical examples of using the `ls` command:

1. **Basic Listing**
   ```bash
   ls
   ```

2. **Detailed Listing**
   ```bash
   ls -l
   ```

3. **Including Hidden Files**
   ```bash
   ls -a
   ```

4. **Human-Readable Sizes**
   ```bash
   ls -lh
   ```

5. **Recursive Listing**
   ```bash
   ls -R
   ```

6. **Sorting by Modification Time**
   ```bash
   ls -lt
   ```

7. **Sorting by Size**
   ```bash
   ls -lS
   ```

## Tips
- Combine options for more powerful listings. For example, `ls -la` will show all files with detailed information.
- Use `ls` in scripts to check for the presence of files or directories.
- Remember that the output of `ls` can be piped to other commands for further processing, such as `grep` for filtering specific files.