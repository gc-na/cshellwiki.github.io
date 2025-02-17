# [Linux] Bash lvextend uso equivalente: Extend logical volumes

## Overview
The `lvextend` command is used in Linux to increase the size of a logical volume in a volume group. This is particularly useful when you need to allocate more space to a filesystem that is running out of space.

## Usage
The basic syntax of the `lvextend` command is as follows:

```bash
lvextend [options] [arguments]
```

## Common Options
- `-L +size`: Increase the size of the logical volume by the specified amount (e.g., `+10G` to add 10 gigabytes).
- `-L size`: Set the logical volume to the specified size (e.g., `20G` to resize it to 20 gigabytes).
- `-r`: Automatically resize the filesystem on the logical volume after extending it.
- `-n name`: Change the name of the logical volume.
- `-v`: Enable verbose output to provide more details during the operation.

## Common Examples
Here are some practical examples of using the `lvextend` command:

1. **Extend a logical volume by 5GB:**
   ```bash
   lvextend -L +5G /dev/vg_name/lv_name
   ```

2. **Set a logical volume to a specific size of 30GB:**
   ```bash
   lvextend -L 30G /dev/vg_name/lv_name
   ```

3. **Extend a logical volume and resize the filesystem automatically:**
   ```bash
   lvextend -r -L +10G /dev/vg_name/lv_name
   ```

4. **Extend a logical volume with verbose output:**
   ```bash
   lvextend -v -L +15G /dev/vg_name/lv_name
   ```

## Tips
- Always ensure you have a backup of important data before resizing logical volumes.
- Use the `-r` option whenever possible to avoid the need for a separate filesystem resize command.
- Check the available space in the volume group with `vgs` before extending a logical volume to ensure there is enough space.
- After extending a logical volume, verify the new size using `lvdisplay` or `df -h` to confirm the changes.