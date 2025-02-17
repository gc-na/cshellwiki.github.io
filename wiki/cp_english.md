# [Linux] Bash cp Uso equivalente: Copy files and directories

The `cp` command is used to copy files and directories in a Linux environment.

## Overview
The `cp` command allows users to create copies of files and directories. It can be used to duplicate files, move files to different locations, or create backups.

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
- `-a`: Archive mode; it preserves the attributes of files and copies directories recursively.

## Common Examples
1. **Copy a single file:**
   ```bash
   cp file.txt /path/to/destination/
   ```

2. **Copy a directory recursively:**
   ```bash
   cp -r /source/directory /path/to/destination/
   ```

3. **Copy a file and prompt before overwriting:**
   ```bash
   cp -i file.txt /path/to/destination/
   ```

4. **Copy only newer files:**
   ```bash
   cp -u file.txt /path/to/destination/
   ```

5. **Copy with verbose output:**
   ```bash
   cp -v file.txt /path/to/destination/
   ```

## Tips
- Always use the `-i` option when copying files to avoid accidental overwrites.
- Use the `-r` option when copying directories to ensure all contents are included.
- Consider using the `-a` option for backups to preserve file attributes.
- Check the destination path before executing the command to prevent copying files to unintended locations.