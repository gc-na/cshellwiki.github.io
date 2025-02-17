# [Linux] Bash update-rc.d Uso: Manage system service start/stop links

## Overview
The `update-rc.d` command is used in Debian-based Linux distributions to manage the symbolic links for system services in the `/etc/rc*.d` directories. This command allows you to add, remove, or modify the startup behavior of services during system boot and shutdown.

## Usage
The basic syntax of the `update-rc.d` command is as follows:

```bash
update-rc.d [options] [service] [defaults|remove]
```

## Common Options
- `defaults`: Adds the service to the default runlevels.
- `remove`: Removes the service from the runlevels.
- `enable`: Enables the service for the specified runlevels.
- `disable`: Disables the service for the specified runlevels.
- `force`: Forces the operation, even if it may not be safe.

## Common Examples

### Adding a Service
To add a service to the default runlevels, you can use the following command:

```bash
update-rc.d myservice defaults
```

### Removing a Service
To remove a service from the runlevels, use:

```bash
update-rc.d myservice remove
```

### Enabling a Service
To enable a service for specific runlevels, you can specify the runlevels like this:

```bash
update-rc.d myservice enable
```

### Disabling a Service
To disable a service, you can run:

```bash
update-rc.d myservice disable
```

### Forcing an Operation
If you need to forcefully add a service, you can use the `force` option:

```bash
update-rc.d myservice defaults force
```

## Tips
- Always check the current status of a service before modifying it to avoid accidental disruptions.
- Use the `--verbose` option to get detailed output of what the command is doing.
- Be cautious when using the `force` option, as it may lead to unexpected behavior if the service is not properly configured.