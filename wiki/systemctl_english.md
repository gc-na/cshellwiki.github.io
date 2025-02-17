# [Linux] Bash systemctl Uso: Manage system services

## Overview
The `systemctl` command is a powerful tool used in Linux systems to manage system services and the system's overall state. It is part of the systemd system and service manager, allowing users to start, stop, enable, disable, and check the status of services.

## Usage
The basic syntax of the `systemctl` command is as follows:

```bash
systemctl [options] [arguments]
```

## Common Options
- `start`: Starts a specified service.
- `stop`: Stops a specified service.
- `restart`: Restarts a specified service.
- `status`: Displays the current status of a specified service.
- `enable`: Enables a service to start automatically at boot.
- `disable`: Prevents a service from starting automatically at boot.
- `list-units`: Lists all loaded units (services, sockets, etc.).
- `is-active`: Checks if a specified service is currently active.

## Common Examples
Here are some practical examples of using the `systemctl` command:

1. **Start a service**:
   ```bash
   systemctl start apache2
   ```

2. **Stop a service**:
   ```bash
   systemctl stop apache2
   ```

3. **Restart a service**:
   ```bash
   systemctl restart apache2
   ```

4. **Check the status of a service**:
   ```bash
   systemctl status apache2
   ```

5. **Enable a service to start at boot**:
   ```bash
   systemctl enable apache2
   ```

6. **Disable a service from starting at boot**:
   ```bash
   systemctl disable apache2
   ```

7. **List all active services**:
   ```bash
   systemctl list-units --type=service
   ```

8. **Check if a service is active**:
   ```bash
   systemctl is-active apache2
   ```

## Tips
- Always check the status of a service after starting or stopping it to ensure it behaves as expected.
- Use `systemctl list-units --type=service` to get an overview of all services and their states.
- When enabling services, be mindful of dependencies that might affect the boot process.
- For troubleshooting, check the logs using `journalctl -u [service_name]` to get detailed information about service activity.