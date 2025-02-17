# [Linux] Bash parted Usage: Manage disk partitions

## Overview
The `parted` command is a powerful tool used in Linux for managing disk partitions. It allows users to create, delete, resize, and manipulate disk partitions on various storage devices. `parted` supports both MBR (Master Boot Record) and GPT (GUID Partition Table) partitioning schemes, making it versatile for different systems.

## Usage
The basic syntax of the `parted` command is as follows:

```bash
parted [options] [arguments]
```

## Common Options
- `-s`, `--script`: Run in script mode, suppressing all interactive prompts.
- `-m`, `--machine`: Output in a machine-readable format.
- `--version`: Display the version of `parted`.
- `--help`: Show help information about the command and its options.

## Common Examples

### Start parted with a specific device
To start `parted` on a specific disk (e.g., `/dev/sda`):

```bash
parted /dev/sda
```

### Create a new partition
To create a new partition of 10GB on `/dev/sda` starting at 1GB:

```bash
parted /dev/sda mkpart primary ext4 1GB 11GB
```

### Resize a partition
To resize an existing partition (e.g., partition 1) to 20GB:

```bash
parted /dev/sda resizepart 1 20GB
```

### Delete a partition
To delete partition 2 on `/dev/sda`:

```bash
parted /dev/sda rm 2
```

### Print the partition table
To display the current partition layout of the disk:

```bash
parted /dev/sda print
```

## Tips
- Always back up important data before modifying partitions to prevent data loss.
- Use the `-s` option when running scripts to avoid interactive prompts that can halt automated processes.
- Familiarize yourself with the partitioning scheme (MBR or GPT) of your disk to avoid compatibility issues.
- Use `print` frequently to check your changes and ensure everything is as expected before finalizing any operations.