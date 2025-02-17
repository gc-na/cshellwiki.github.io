# [Linux] Bash df Uso equivalente: Display disk space usage

## Overview
The `df` command in Bash is used to display information about disk space usage on file systems. It provides a summary of available and used disk space, helping users monitor their storage capacity.

## Usage
The basic syntax of the `df` command is as follows:

```bash
df [options] [arguments]
```

## Common Options
- `-h`: Displays the output in a human-readable format (e.g., in KB, MB, or GB).
- `-T`: Shows the file system type along with the disk space usage.
- `-a`: Includes dummy file systems in the output.
- `-i`: Displays information about inodes instead of block usage.

## Common Examples

1. **Basic Disk Space Usage**
   To display the disk space usage of all mounted file systems:
   ```bash
   df
   ```

2. **Human-Readable Format**
   To show the disk space in a more understandable format:
   ```bash
   df -h
   ```

3. **Including File System Type**
   To display the file system type along with usage:
   ```bash
   df -T
   ```

4. **Checking Inodes Usage**
   To see inode usage instead of block usage:
   ```bash
   df -i
   ```

5. **Including All File Systems**
   To include all file systems, even those that are not currently mounted:
   ```bash
   df -a
   ```

## Tips
- Use the `-h` option for easier readability, especially when dealing with large disk sizes.
- Combine options for more detailed output, such as `df -hT` to see both human-readable sizes and file system types.
- Regularly check disk usage to avoid running out of space, which can cause system issues.