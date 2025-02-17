# [Linux] Bash hwclock用法: Manage Hardware Clock

## Overview
The `hwclock` command is used to access and manage the hardware clock (RTC - Real Time Clock) on a Linux system. This clock keeps track of the current time even when the system is powered off, ensuring accurate timekeeping.

## Usage
The basic syntax of the `hwclock` command is as follows:

```bash
hwclock [options] [arguments]
```

## Common Options
- `--show`: Display the current hardware clock time.
- `--set`: Set the hardware clock to a specified time.
- `--hctosys`: Set the system time from the hardware clock.
- `--systohc`: Set the hardware clock to the current system time.
- `--utc`: Treat the hardware clock as UTC (Coordinated Universal Time).
- `--localtime`: Treat the hardware clock as local time.

## Common Examples

1. **Display the current hardware clock time:**
   ```bash
   hwclock --show
   ```

2. **Set the hardware clock to a specific date and time:**
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

3. **Set the system time from the hardware clock:**
   ```bash
   hwclock --hctosys
   ```

4. **Set the hardware clock to the current system time:**
   ```bash
   hwclock --systohc
   ```

5. **Display the hardware clock time in UTC:**
   ```bash
   hwclock --show --utc
   ```

## Tips
- Always ensure that your system time is correct before using `--systohc` to avoid discrepancies between the hardware and system clocks.
- Use the `--utc` option if you are dual-booting with another operating system that uses UTC for the hardware clock.
- Regularly check your hardware clock, especially if your system is powered off for extended periods, to ensure accurate timekeeping.