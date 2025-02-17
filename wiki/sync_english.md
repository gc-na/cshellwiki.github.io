# [Linux] Bash sync uso: Synchronize cached writes to persistent storage

## Overview
The `sync` command in Bash is used to flush file system buffers, ensuring that all data written to disk is properly saved. This is particularly useful when you want to make sure that any changes made to files are reflected on the storage device, especially before shutting down or unmounting a filesystem.

## Usage
The basic syntax of the `sync` command is as follows:

```bash
sync [options] [arguments]
```

Typically, `sync` does not require any arguments or options, as its primary function is to flush the buffers.

## Common Options
While `sync` is straightforward and does not have many options, here are a couple of relevant ones:

- `-f`, `--file`: Synchronize a specific file instead of all buffers.
- `-a`, `--all`: Synchronize all filesystems.

## Common Examples

1. **Basic Usage**
   To flush all file system buffers:
   ```bash
   sync
   ```

2. **Synchronizing a Specific File**
   To synchronize a specific file, you can use:
   ```bash
   sync /path/to/your/file.txt
   ```

3. **Synchronizing All Filesystems**
   To ensure all filesystems are synchronized, you can use:
   ```bash
   sync --all
   ```

4. **Using with Other Commands**
   It's common to use `sync` before unmounting a filesystem to ensure all data is written:
   ```bash
   sync && umount /mnt/usb
   ```

## Tips
- Always run `sync` before shutting down your system to prevent data loss.
- If you're working with external drives, use `sync` after copying files to ensure all data is written before unplugging the drive.
- Consider using `sync` in scripts where data integrity is critical, especially after writing large files.