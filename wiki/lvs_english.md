# [Linux] Bash lvs uso equivalente: List logical volumes

## Overview
The `lvs` command is used in Linux to display information about logical volumes in the Logical Volume Manager (LVM). It provides a concise overview of the logical volumes present on the system, including their size, attributes, and associated volume groups.

## Usage
The basic syntax of the `lvs` command is as follows:

```bash
lvs [options] [arguments]
```

## Common Options
- `-o, --units`: Specify the units for displaying sizes (e.g., k, m, g).
- `-a, --all`: Show all logical volumes, including those that are not active.
- `-n, --noheadings`: Suppress the header line in the output.
- `-f, --full`: Show full information for each logical volume.
- `-S, --select`: Filter the output based on specific criteria.

## Common Examples
Here are some practical examples of using the `lvs` command:

1. **Display all logical volumes:**
   ```bash
   lvs
   ```

2. **Show logical volumes with sizes in gigabytes:**
   ```bash
   lvs -o +size --units g
   ```

3. **List all logical volumes, including inactive ones:**
   ```bash
   lvs -a
   ```

4. **Display logical volumes without headers:**
   ```bash
   lvs -n
   ```

5. **Filter logical volumes by a specific volume group:**
   ```bash
   lvs -S 'vg_name=your_volume_group'
   ```

## Tips
- Use the `-o` option to customize the output and include additional fields that may be relevant to your needs.
- Regularly check your logical volumes to monitor their usage and ensure they are functioning correctly.
- Combine `lvs` with other LVM commands like `lvcreate` and `lvremove` for effective volume management.