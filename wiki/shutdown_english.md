# [Linux] Bash shutdown uso: Shut down or restart the system

## Overview
The `shutdown` command in Bash is used to turn off or restart a computer safely. It allows users to schedule a shutdown or reboot, ensuring that all processes are terminated properly and that data is saved.

## Usage
The basic syntax of the `shutdown` command is as follows:

```bash
shutdown [options] [time] [message]
```

## Common Options
- `-h` or `--halt`: Halts the system after shutdown.
- `-r` or `--reboot`: Reboots the system after shutdown.
- `-P` or `--poweroff`: Powers off the system after shutdown.
- `now`: Specifies that the shutdown should occur immediately.
- `+m`: Schedules a shutdown in `m` minutes.
- `hh:mm`: Schedules a shutdown at a specific time.

## Common Examples
Here are some practical examples of how to use the `shutdown` command:

1. **Immediate Shutdown:**
   ```bash
   shutdown now
   ```

2. **Scheduled Shutdown in 10 Minutes:**
   ```bash
   shutdown +10
   ```

3. **Reboot the System Immediately:**
   ```bash
   shutdown -r now
   ```

4. **Shutdown at a Specific Time (e.g., 10:30 PM):**
   ```bash
   shutdown 22:30
   ```

5. **Shutdown with a Custom Message:**
   ```bash
   shutdown +5 "System will shut down in 5 minutes. Please save your work."
   ```

## Tips
- Always inform users about an impending shutdown by including a message.
- Use the `-h` option if you want to halt the system without rebooting.
- To cancel a scheduled shutdown, use the command `shutdown -c`.
- Consider using `shutdown -r` for maintenance tasks that require a reboot after updates.