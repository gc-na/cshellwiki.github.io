# [Linux] Bash blkid Uso equivalente: Retrieve block device attributes

## Overview
The `blkid` command in Bash is used to locate and display block device attributes, such as the filesystem type, label, and UUID (Universally Unique Identifier) of storage devices. This command is particularly useful for system administrators and users who need to manage disk partitions and filesystems.

## Usage
The basic syntax of the `blkid` command is as follows:

```bash
blkid [options] [arguments]
```

## Common Options
- `-o, --output <format>`: Specify the output format (e.g., `value`, `full`, `list`).
- `-s, --match-tag <tag>`: Show only the specified tag (e.g., `UUID`, `TYPE`).
- `-p, --probe`: Probe devices for their attributes.
- `-c, --cache <file>`: Use a specified cache file instead of the default.
- `-h, --help`: Display help information about the command.

## Common Examples

### Display all block devices
To list all block devices along with their attributes, simply run:
```bash
blkid
```

### Show UUID of a specific device
To retrieve the UUID of a specific device, use:
```bash
blkid /dev/sda1
```

### Output only the UUID
If you want to display only the UUID of a device, you can use the `-s` option:
```bash
blkid -s UUID /dev/sda1
```

### List devices with a specific filesystem type
To filter the output to show only devices with a specific filesystem type, you can combine options:
```bash
blkid -t TYPE=ext4
```

### Custom output format
To customize the output format to show only the labels of the devices, you can use:
```bash
blkid -o value -s LABEL
```

## Tips
- Use `blkid` without any arguments to quickly see all available block devices and their attributes.
- When scripting, consider using the `-o value` option to make parsing the output easier.
- If you frequently use `blkid`, check if your system supports caching to speed up subsequent queries.