# [Linux] Bash lsmod Uso: Display loaded kernel modules

## Overview
The `lsmod` command is used in Linux to display the status of modules that are currently loaded into the kernel. It provides a list of all active modules, along with their sizes and dependencies, which can be useful for troubleshooting and system management.

## Usage
The basic syntax of the `lsmod` command is as follows:

```bash
lsmod [options] [arguments]
```

## Common Options
While `lsmod` does not have many options, here are a few that can be useful:

- **-h, --help**: Display help information about the command.
- **-v, --version**: Show the version of the `lsmod` command.

## Common Examples

1. **Display all loaded modules**:
   To simply list all currently loaded kernel modules, use:
   ```bash
   lsmod
   ```

2. **Display help information**:
   If you need help with the command, you can run:
   ```bash
   lsmod --help
   ```

3. **Check the version**:
   To find out the version of the `lsmod` command, use:
   ```bash
   lsmod --version
   ```

## Tips
- Use `lsmod` in combination with other commands like `modinfo` to get detailed information about specific modules.
- Regularly check loaded modules if you are troubleshooting hardware issues, as it can help identify missing or problematic drivers.
- Keep in mind that `lsmod` only shows modules that are currently loaded; it does not list available modules that are not loaded. For that, consider using `modprobe -l`.