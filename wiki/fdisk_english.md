# [Linux] Bash fdisk Uso: Manage disk partitions

## Overview
The `fdisk` command is a powerful utility used for managing disk partitions in Linux. It allows users to create, delete, resize, and manipulate disk partitions on hard drives and other storage devices.

## Usage
The basic syntax of the `fdisk` command is as follows:

```bash
fdisk [options] [device]
```

Where `[device]` is typically the path to the disk you want to manage (e.g., `/dev/sda`).

## Common Options
- `-l`: List all available partitions on all disks.
- `-u`: Use sectors instead of cylinders for displaying partition sizes.
- `-n`: Create a new partition.
- `-d`: Delete a partition.
- `-p`: Print the partition table of the specified device.
- `-s`: Display the size of a partition.

## Common Examples
1. **List all partitions on all disks:**
   ```bash
   fdisk -l
   ```

2. **View the partition table of a specific disk:**
   ```bash
   fdisk -p /dev/sda
   ```

3. **Create a new partition:**
   ```bash
   fdisk /dev/sda
   ```
   (Follow the interactive prompts to create a new partition.)

4. **Delete a partition:**
   ```bash
   fdisk /dev/sda
   ```
   (Use the interactive mode to select and delete a partition.)

5. **Display the size of a specific partition:**
   ```bash
   fdisk -s /dev/sda1
   ```

## Tips
- Always back up important data before modifying disk partitions to prevent data loss.
- Use `parted` or `gparted` for a more user-friendly graphical interface if you're not comfortable with command-line tools.
- Be cautious when deleting partitions, as this action is irreversible and can result in data loss.