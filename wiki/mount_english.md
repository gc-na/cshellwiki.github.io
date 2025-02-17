# [Linux] Bash mount uso: Mount file systems in Linux

## Overview
The `mount` command in Linux is used to attach file systems to a specified directory in the file system hierarchy. This allows users to access files and directories stored on different devices or partitions as if they were part of the main file system.

## Usage
The basic syntax of the `mount` command is as follows:

```bash
mount [options] [device] [mount_point]
```

- **device**: The storage device or partition you want to mount.
- **mount_point**: The directory where the file system will be attached.

## Common Options
- `-t fstype`: Specify the type of file system (e.g., ext4, ntfs).
- `-o options`: Specify mount options (e.g., read-only, noexec).
- `-a`: Mount all file systems mentioned in `/etc/fstab`.
- `-r`: Mount the file system as read-only.
- `-v`: Verbose output, showing detailed information during the mount process.

## Common Examples

### Mounting a USB Drive
To mount a USB drive located at `/dev/sdb1` to the directory `/mnt/usb`, you can use:

```bash
sudo mount /dev/sdb1 /mnt/usb
```

### Mounting with a Specific File System Type
If you know the file system type of the device, you can specify it. For example, to mount an NTFS drive:

```bash
sudo mount -t ntfs /dev/sdc1 /mnt/ntfs_drive
```

### Mounting with Options
To mount a file system as read-only, you can use the `-o` option:

```bash
sudo mount -o ro /dev/sda1 /mnt/read_only
```

### Mounting All File Systems
To mount all file systems listed in `/etc/fstab`, simply use:

```bash
sudo mount -a
```

## Tips
- Always ensure that the mount point directory exists before mounting. You can create it using `mkdir /mnt/my_mount_point`.
- Use `df -h` to check mounted file systems and their usage.
- To unmount a file system, use the `umount` command followed by the mount point or device name.
- Be cautious when mounting file systems, especially with write permissions, to avoid data loss.