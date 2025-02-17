# [Linux] Bash pkg uso: Package management command

## Overview
The `pkg` command is a package management tool used primarily in FreeBSD and some other Unix-like operating systems. It simplifies the process of installing, upgrading, and managing software packages from repositories.

## Usage
The basic syntax of the `pkg` command is as follows:

```bash
pkg [options] [arguments]
```

## Common Options
- `install`: Installs a package.
- `remove`: Uninstalls a package.
- `upgrade`: Upgrades installed packages to their latest versions.
- `search`: Searches for a package in the repositories.
- `info`: Displays information about a specific package.
- `list`: Lists all installed packages.

## Common Examples
Here are some practical examples of using the `pkg` command:

### Installing a Package
To install a package, use the `install` option followed by the package name:

```bash
pkg install vim
```

### Removing a Package
To uninstall a package, use the `remove` option:

```bash
pkg remove vim
```

### Upgrading Packages
To upgrade all installed packages to their latest versions, use the `upgrade` option:

```bash
pkg upgrade
```

### Searching for a Package
To search for a package by name, use the `search` option:

```bash
pkg search nginx
```

### Getting Package Information
To display detailed information about a specific package, use the `info` option:

```bash
pkg info vim
```

### Listing Installed Packages
To list all currently installed packages, use the `list` option:

```bash
pkg list
```

## Tips
- Always update your package repository database before installing or upgrading packages by running `pkg update`.
- Use the `-y` flag with install or remove commands to automatically confirm prompts (e.g., `pkg install -y vim`).
- Check for outdated packages regularly with `pkg version -l '<'` to ensure your system is up to date.