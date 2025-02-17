# [Linux] Bash swapon Usage: Enable swap space

## Overview
The `swapon` command in Linux is used to enable devices and files for paging and swapping. It allows the operating system to use additional memory resources, which can help improve performance when the physical RAM is full.

## Usage
The basic syntax of the `swapon` command is as follows:

```bash
swapon [options] [arguments]
```

## Common Options
- `-a`: Enables all swap devices listed in `/etc/fstab`.
- `-e`: Ignores errors when enabling swap devices.
- `-s`: Displays summary information about swap space.
- `--show`: Similar to `-s`, but provides more detailed output.

## Common Examples

1. **Enable all swap devices:**
   To enable all swap devices defined in the `/etc/fstab` file, you can use:
   ```bash
   swapon -a
   ```

2. **Enable a specific swap file:**
   If you have a specific swap file (e.g., `/swapfile`) that you want to enable, you can do so with:
   ```bash
   swapon /swapfile
   ```

3. **Display current swap usage:**
   To see a summary of the currently active swap space, use:
   ```bash
   swapon --show
   ```

4. **Enable swap with error ignoring:**
   If you want to enable a swap device and ignore any errors that might occur, you can run:
   ```bash
   swapon -e /dev/sdX
   ```

## Tips
- Always check your swap space after enabling it with `swapon --show` to ensure it's active.
- Consider using `swapon -a` during system startup by adding it to your initialization scripts for automatic swap management.
- Monitor your system's memory usage to determine if you need to adjust your swap space settings.