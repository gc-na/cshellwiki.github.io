# [Linux] Bash tune2fs Usage: Adjust ext2/ext3/ext4 filesystem parameters

## Overview
The `tune2fs` command is used to adjust tunable filesystem parameters on ext2, ext3, and ext4 filesystems. It allows users to modify various filesystem settings without needing to unmount the filesystem, making it a powerful tool for system administrators.

## Usage
The basic syntax of the `tune2fs` command is as follows:

```bash
tune2fs [options] [arguments]
```

## Common Options
- `-c <max_mount_count>`: Set the maximum number of times the filesystem can be mounted before a check is forced.
- `-i <interval>`: Set the maximum time interval between filesystem checks.
- `-O <feature>`: Enable specific filesystem features.
- `-o <options>`: Set filesystem options.
- `-l`: List the current parameters of the filesystem.
- `-e <error_behavior>`: Set the behavior when an error is detected.

## Common Examples
Here are some practical examples of using `tune2fs`:

1. **List current filesystem parameters**:
   ```bash
   tune2fs -l /dev/sda1
   ```

2. **Set maximum mount count to 20**:
   ```bash
   tune2fs -c 20 /dev/sda1
   ```

3. **Set the maximum time between checks to 30 days**:
   ```bash
   tune2fs -i 30d /dev/sda1
   ```

4. **Enable the `dir_index` feature**:
   ```bash
   tune2fs -O dir_index /dev/sda1
   ```

5. **Change error behavior to remount read-only**:
   ```bash
   tune2fs -e remount-ro /dev/sda1
   ```

## Tips
- Always back up important data before modifying filesystem parameters.
- Use `tune2fs` with caution, as incorrect settings can lead to filesystem issues.
- Regularly check and adjust your filesystem parameters based on usage patterns to maintain optimal performance.