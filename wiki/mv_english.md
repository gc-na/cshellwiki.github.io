# [Linux] Bash mv Uso equivalente: Move or rename files and directories

## Overview
The `mv` command in Bash is used to move or rename files and directories. It is a fundamental command in Unix-like operating systems, allowing users to organize their file systems efficiently.

## Usage
The basic syntax of the `mv` command is as follows:

```bash
mv [options] [source] [destination]
```

- **source**: The file or directory you want to move or rename.
- **destination**: The new location or name for the file or directory.

## Common Options
- `-i`: Prompts before overwriting an existing file.
- `-u`: Moves files only when the source file is newer than the destination file or when the destination file is missing.
- `-v`: Verbose mode; displays the files being moved.
- `-n`: Prevents overwriting existing files.

## Common Examples
Here are some practical examples of using the `mv` command:

### Move a file to a different directory
```bash
mv file.txt /path/to/destination/
```

### Rename a file
```bash
mv oldname.txt newname.txt
```

### Move multiple files to a directory
```bash
mv file1.txt file2.txt /path/to/destination/
```

### Move a directory
```bash
mv /path/to/source_directory /path/to/destination_directory/
```

### Move a file with a prompt before overwriting
```bash
mv -i file.txt /path/to/destination/
```

## Tips
- Always double-check the destination path to avoid accidental data loss.
- Use the `-v` option for a clearer understanding of what files are being moved, especially when moving multiple files.
- Consider using the `-n` option when moving files to prevent overwriting existing files unintentionally.