# [Linux] Bash chkconfig Usage: Manage System Services

## Overview
The `chkconfig` command is used in Linux systems to manage the system services that run at different run levels. It allows users to easily enable or disable services and view their status across various run levels.

## Usage
The basic syntax of the `chkconfig` command is as follows:

```bash
chkconfig [options] [service] [on|off|reset]
```

## Common Options
- `--list`: Displays the status of all services.
- `--add`: Adds a new service to the chkconfig system.
- `--del`: Removes a service from the chkconfig system.
- `--level`: Specifies the run levels to apply the command (e.g., `--level 2345`).
- `--set`: Sets the specified service to the desired run level.

## Common Examples

1. **List all services and their status:**
   ```bash
   chkconfig --list
   ```

2. **Enable a service to start at boot:**
   ```bash
   chkconfig httpd on
   ```

3. **Disable a service from starting at boot:**
   ```bash
   chkconfig httpd off
   ```

4. **Add a new service to chkconfig:**
   ```bash
   chkconfig --add myservice
   ```

5. **Remove a service from chkconfig:**
   ```bash
   chkconfig --del myservice
   ```

6. **Set a service to specific run levels:**
   ```bash
   chkconfig --level 2345 myservice on
   ```

## Tips
- Always check the status of services after making changes to ensure they are set as intended.
- Use the `--level` option carefully to avoid enabling services in run levels where they are not needed.
- Consider using `service` command for starting or stopping services immediately, while `chkconfig` is more about their boot-time configuration.