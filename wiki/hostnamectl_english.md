# [Linux] Bash hostnamectl Uso: Manage system hostname and related settings

## Overview
The `hostnamectl` command is used in Linux systems to manage the system's hostname and related settings. It allows users to view and change the hostname, as well as configure other related parameters like the operating system name and version.

## Usage
The basic syntax of the `hostnamectl` command is as follows:

```bash
hostnamectl [options] [arguments]
```

## Common Options
- `set-hostname`: Change the system's hostname.
- `status`: Display the current hostname and related information.
- `set-icon-name`: Set an icon name for the system.
- `set-chassis`: Specify the type of hardware chassis (e.g., desktop, laptop).
- `set-deployment`: Define the deployment type (e.g., production, development).

## Common Examples

### 1. Display Current Hostname
To view the current hostname and related information, use:

```bash
hostnamectl status
```

### 2. Change the Hostname
To change the hostname to "new-hostname", run:

```bash
sudo hostnamectl set-hostname new-hostname
```

### 3. Set Chassis Type
To specify the chassis type as "laptop", use:

```bash
sudo hostnamectl set-chassis laptop
```

### 4. Set Icon Name
To set an icon name for the system, you can use:

```bash
sudo hostnamectl set-icon-name computer-laptop
```

### 5. View All Hostname Information
To get a comprehensive view of the hostname and system information, execute:

```bash
hostnamectl
```

## Tips
- Always use `sudo` when changing the hostname to ensure you have the necessary permissions.
- After changing the hostname, consider rebooting the system for all services to recognize the new name.
- Use descriptive hostnames that reflect the purpose or location of the machine for easier management in larger networks.