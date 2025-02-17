# [Linux] Bash lsblk Uso equivalente: Listar dispositivos de bloque

## Overview
The `lsblk` command is used in Linux to list information about all available or specified block devices. It provides a tree-like structure that shows the relationships between devices, making it easier to understand how storage devices are organized.

## Usage
The basic syntax of the `lsblk` command is as follows:

```bash
lsblk [options] [arguments]
```

## Common Options
- `-a`, `--all`: Show all devices, including empty ones.
- `-f`, `--fs`: Display filesystem information along with the device details.
- `-l`, `--list`: Use a list format instead of the tree format.
- `-n`, `--noheadings`: Suppress the header output.
- `-o`, `--output`: Specify which columns to display in the output.
- `-p`, `--paths`: Print the device paths instead of the device names.

## Common Examples
Here are some practical examples of using the `lsblk` command:

### Example 1: Basic usage
To list all block devices in a tree format:
```bash
lsblk
```

### Example 2: List all devices with filesystem information
To show detailed information about each device, including filesystem type:
```bash
lsblk -f
```

### Example 3: List devices in a simple list format
To display devices in a list format:
```bash
lsblk -l
```

### Example 4: Suppress headers
To list devices without headers:
```bash
lsblk -n
```

### Example 5: Specify output columns
To customize the output to show only the NAME and SIZE columns:
```bash
lsblk -o NAME,SIZE
```

## Tips
- Use `lsblk` in combination with other commands like `grep` to filter specific devices.
- Regularly check your block devices to monitor disk usage and available space.
- Use the `-p` option if you need to work with device paths in scripts or commands.