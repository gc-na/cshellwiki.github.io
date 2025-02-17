# [Linux] Bash flatpak uso: Manage and run applications in a sandboxed environment

## Overview
The `flatpak` command is a tool used to manage and run applications in a sandboxed environment on Linux systems. It allows users to install, update, and remove applications that are packaged in a way that isolates them from the rest of the system, enhancing security and compatibility.

## Usage
The basic syntax of the `flatpak` command is as follows:

```bash
flatpak [options] [arguments]
```

## Common Options
- `install`: Installs a specified application.
- `uninstall`: Removes a specified application.
- `update`: Updates installed applications to their latest versions.
- `list`: Lists installed applications.
- `run`: Runs a specified application.
- `info`: Displays information about a specified application.

## Common Examples
Here are some practical examples of using the `flatpak` command:

### Install an Application
To install an application, use the `install` option followed by the application name:

```bash
flatpak install flathub org.videolan.VLC
```

### Uninstall an Application
To remove an installed application, use the `uninstall` option:

```bash
flatpak uninstall org.videolan.VLC
```

### Update Installed Applications
To update all installed applications to their latest versions, use the `update` option:

```bash
flatpak update
```

### List Installed Applications
To see a list of all installed applications, use the `list` option:

```bash
flatpak list
```

### Run an Application
To run a specific application, use the `run` option followed by the application name:

```bash
flatpak run org.videolan.VLC
```

### Get Information About an Application
To view detailed information about a specific application, use the `info` option:

```bash
flatpak info org.videolan.VLC
```

## Tips
- Always check for updates regularly to ensure your applications are secure and up-to-date.
- Use the `flatpak search [application_name]` command to find applications available for installation.
- Consider using the `--user` option when installing applications to install them only for your user account, avoiding system-wide changes.