# [Linux] Bash timedatectl Uso: Manage system time and date settings

## Overview
The `timedatectl` command is a utility in Linux that allows users to query and change the system clock and its settings. It provides a straightforward interface to manage time zones, synchronize time with network time servers, and display the current date and time.

## Usage
The basic syntax of the `timedatectl` command is as follows:

```bash
timedatectl [options] [arguments]
```

## Common Options
- `set-time`: Set the system time.
- `set-timezone`: Change the system time zone.
- `set-ntp`: Enable or disable NTP (Network Time Protocol) synchronization.
- `status`: Show the current time settings and status.
- `list-timezones`: Display a list of available time zones.

## Common Examples

### Display Current Time and Date
To check the current time and date settings, use:

```bash
timedatectl status
```

### Set System Time
To set the system time to a specific value, use:

```bash
timedatectl set-time '2023-10-01 12:00:00'
```

### Change Time Zone
To change the system time zone, for example to 'America/New_York', use:

```bash
timedatectl set-timezone America/New_York
```

### Enable NTP Synchronization
To enable automatic time synchronization with NTP servers, use:

```bash
timedatectl set-ntp true
```

### List Available Time Zones
To see a list of all available time zones, use:

```bash
timedatectl list-timezones
```

## Tips
- Always check the current time settings with `timedatectl status` before making changes.
- Use the `list-timezones` option to find the correct time zone name for your location.
- Remember that changing the system time may affect scheduled tasks and services that rely on accurate timekeeping.