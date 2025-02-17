# [Linux] Bash pvs Uso equivalente: Display information about LVM physical volumes

## Overview
The `pvs` command is a part of the Logical Volume Manager (LVM) suite in Linux. It is used to display information about physical volumes in the LVM system, including their size, allocation, and status. This command is particularly useful for system administrators managing storage in a Linux environment.

## Usage
The basic syntax of the `pvs` command is as follows:

```bash
pvs [options] [arguments]
```

## Common Options
- `-o, --options`: Specify which columns to display.
- `-h, --no-heading`: Suppress the header line in the output.
- `--units`: Display sizes in specified units (e.g., MB, GB).
- `-d, --debug`: Enable debug output for troubleshooting.
- `-f, --full`: Show full information about physical volumes.

## Common Examples

1. **Display Basic Information about Physical Volumes**
   ```bash
   pvs
   ```

2. **Display Specific Columns**
   ```bash
   pvs -o +pv_size,pv_free
   ```

3. **Suppress Header in Output**
   ```bash
   pvs --no-heading
   ```

4. **Display Sizes in Gigabytes**
   ```bash
   pvs --units g
   ```

5. **Show Full Information**
   ```bash
   pvs --full
   ```

## Tips
- Use the `-o` option to customize the output to show only the information you need, making it easier to read.
- Combine `pvs` with other LVM commands like `lvdisplay` and `vgdisplay` for comprehensive storage management.
- Regularly check the status of your physical volumes to ensure optimal performance and to identify any potential issues early.