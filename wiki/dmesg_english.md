# [Linux] Bash dmesg Uso: Display kernel-related messages

## Overview
The `dmesg` command is used to print or control the kernel ring buffer, which contains messages related to the system's hardware and kernel events. This command is particularly useful for diagnosing hardware issues and monitoring system performance.

## Usage
The basic syntax of the `dmesg` command is as follows:

```bash
dmesg [options] [arguments]
```

## Common Options
- `-C` : Clear the ring buffer.
- `-c` : Clear the ring buffer after printing its contents.
- `-n level` : Set the level of messages that will be printed.
- `-T` : Print human-readable timestamps.
- `-f facility` : Filter messages by facility (e.g., user, daemon).

## Common Examples
Here are some practical examples of using the `dmesg` command:

1. **Display all kernel messages:**
   ```bash
   dmesg
   ```

2. **Display messages with human-readable timestamps:**
   ```bash
   dmesg -T
   ```

3. **Clear the kernel ring buffer:**
   ```bash
   dmesg -C
   ```

4. **Filter messages to show only those related to the hardware:**
   ```bash
   dmesg | grep -i hardware
   ```

5. **Display messages with a specific severity level (e.g., error):**
   ```bash
   dmesg -n 3
   ```

## Tips
- Use `dmesg | less` to scroll through long output conveniently.
- Combine `dmesg` with `grep` to search for specific keywords, making it easier to find relevant messages.
- Regularly check `dmesg` after system changes or updates to identify any potential issues.