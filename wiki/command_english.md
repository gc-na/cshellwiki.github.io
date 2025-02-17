# [Linux] Bash command cp: Copy files and directories

## Overview
The `cp` command in Bash is used to copy files and directories from one location to another. It allows users to duplicate files or entire directory structures, making it a fundamental tool for file management in Linux and Unix-like operating systems.

## Usage
The basic syntax of the `cp` command is as follows:

```bash
cp [options] [source] [destination]
```

## Common Options
- `-r`: Recursively copy directories and their contents.
- `-i`: Prompt before overwriting files.
- `-u`: Copy only when the source file is newer than the destination file or when the destination file is missing.
- `-v`: Verbosely show the files being copied.
- `-a`: Archive mode; it preserves the file attributes and copies directories recursively.

## Common Examples
Here are some practical examples of using the `cp` command:

1. **Copy a single file:**
   ```bash
   cp file.txt /path/to/destination/
   ```

2. **Copy a directory recursively:**
   ```bash
   cp -r /path/to/source_directory /path/to/destination_directory/
   ```

3. **Copy a file with confirmation before overwriting:**
   ```bash
   cp -i file.txt /path/to/destination/
   ```

4. **Copy only newer files:**
   ```bash
   cp -u file.txt /path/to/destination/
   ```

5. **Copy a file and show the progress:**
   ```bash
   cp -v file.txt /path/to/destination/
   ```

## Tips
- Always use the `-i` option when copying files to avoid accidentally overwriting important files.
- When copying large directories, consider using the `-v` option to monitor the progress of the operation.
- If you need to preserve file permissions and timestamps, use the `-a` option to ensure an accurate copy.
- For copying files across different file systems, ensure that the destination has enough space to accommodate the copied files.