# [Linux] Bash lvm usage: Manage Logical Volumes

## Overview
The `lvm` command is used to manage Logical Volume Management (LVM) in Linux. It allows users to create, resize, and manage disk partitions in a flexible manner, making it easier to allocate storage space as needed.

## Usage
The basic syntax of the `lvm` command is as follows:

```bash
lvm [options] [arguments]
```

## Common Options
- `create`: Create a new logical volume.
- `remove`: Delete a logical volume.
- `resize`: Change the size of a logical volume.
- `activate`: Activate a logical volume.
- `deactivate`: Deactivate a logical volume.
- `display`: Show information about logical volumes.

## Common Examples

### Creating a Logical Volume
To create a new logical volume named `my_volume` of size 10GB in the volume group `my_volume_group`, use:

```bash
lvm create -L 10G -n my_volume my_volume_group
```

### Removing a Logical Volume
To remove the logical volume `my_volume`, use:

```bash
lvm remove my_volume
```

### Resizing a Logical Volume
To resize `my_volume` to 20GB, use:

```bash
lvm resize -L 20G my_volume
```

### Activating a Logical Volume
To activate the logical volume `my_volume`, use:

```bash
lvm activate my_volume
```

### Deactivating a Logical Volume
To deactivate the logical volume `my_volume`, use:

```bash
lvm deactivate my_volume
```

### Displaying Logical Volumes
To display information about all logical volumes, use:

```bash
lvm display
```

## Tips
- Always ensure you have backups of important data before modifying logical volumes.
- Use the `--dry-run` option with commands to preview changes without applying them.
- Regularly check the status of your logical volumes to avoid unexpected issues.
- Familiarize yourself with the LVM documentation for advanced features and options.