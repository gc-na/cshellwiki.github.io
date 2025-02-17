# [Linux] Bash mountpoint Usage: Check if a directory is a mount point

## Overview
The `mountpoint` command is used in Linux to determine whether a specified directory is a mount point for a filesystem. This can be particularly useful for system administrators and users who need to manage mounted filesystems.

## Usage
The basic syntax of the `mountpoint` command is as follows:

```bash
mountpoint [options] [directory]
```

## Common Options
- `-q`: Quiet mode; does not output anything, only sets the exit status.
- `-n`: Treats the directory as a pathname without resolving it to a mount point.
- `--help`: Displays help information about the command.

## Common Examples

1. **Check if a directory is a mount point:**
   ```bash
   mountpoint /mnt/mydrive
   ```
   This command checks if `/mnt/mydrive` is a mount point and outputs the result.

2. **Using quiet mode to check:**
   ```bash
   mountpoint -q /mnt/mydrive
   ```
   This command checks if `/mnt/mydrive` is a mount point without displaying any output. You can check the exit status with `echo $?`.

3. **Check a directory without resolving it:**
   ```bash
   mountpoint -n /mnt/mydrive
   ```
   This command checks if `/mnt/mydrive` is a mount point, treating it as a plain pathname.

4. **Check multiple directories:**
   ```bash
   mountpoint /mnt/mydrive /mnt/otherdrive
   ```
   This command checks if both `/mnt/mydrive` and `/mnt/otherdrive` are mount points and displays the results for each.

## Tips
- Use the `-q` option when you only need to know the status without cluttering your terminal with output.
- Always verify the exit status after using `mountpoint` in scripts to handle different scenarios effectively.
- Remember that a directory can be a mount point even if it is empty, so ensure you check the intended directory correctly.