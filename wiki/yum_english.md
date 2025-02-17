# [Linux] Bash yum Usage: Package management command

## Overview
The `yum` command, short for Yellowdog Updater Modified, is a package management utility for RPM-compatible Linux distributions. It allows users to install, update, remove, and manage software packages from repositories, making it easier to maintain and manage software on the system.

## Usage
The basic syntax of the `yum` command is as follows:

```bash
yum [options] [arguments]
```

## Common Options
Here are some common options you can use with the `yum` command:

- `install`: Installs a specified package.
- `remove`: Uninstalls a specified package.
- `update`: Updates all installed packages to the latest version.
- `search`: Searches for a package by name or description.
- `info`: Displays detailed information about a specified package.
- `list`: Lists available packages or installed packages.
- `clean`: Cleans up cached files to free up space.

## Common Examples
Here are some practical examples of using the `yum` command:

1. **Install a package:**
   ```bash
   yum install httpd
   ```
   This command installs the Apache HTTP Server.

2. **Remove a package:**
   ```bash
   yum remove httpd
   ```
   This command uninstalls the Apache HTTP Server.

3. **Update all installed packages:**
   ```bash
   yum update
   ```
   This command updates all installed packages to their latest versions.

4. **Search for a package:**
   ```bash
   yum search nginx
   ```
   This command searches for packages related to "nginx".

5. **Get information about a package:**
   ```bash
   yum info vim
   ```
   This command displays detailed information about the Vim text editor.

6. **List installed packages:**
   ```bash
   yum list installed
   ```
   This command lists all packages currently installed on the system.

## Tips
- Always run `yum update` regularly to keep your system up to date with the latest security patches and software versions.
- Use `yum clean all` to remove cached files and free up disk space when needed.
- Before removing a package, consider using `yum remove <package> --assumeno` to see what dependencies will be affected without actually removing anything.