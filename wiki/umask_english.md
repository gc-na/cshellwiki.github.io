# [Linux] Bash umask Uso: Set default file permissions

## Overview
The `umask` command in Bash is used to set the default file creation permissions for new files and directories. It defines the permissions that will be removed from the default permissions when a new file or directory is created.

## Usage
The basic syntax of the `umask` command is as follows:

```bash
umask [options] [arguments]
```

## Common Options
- `-S`: Display the current umask value in symbolic format.
- `-p`: Display the current umask value in a format that can be reused in scripts.

## Common Examples

1. **Check Current umask Value**
   To see the current umask value:
   ```bash
   umask
   ```

2. **Set umask to 022**
   This command sets the umask to `022`, which allows the owner to read and write files, while the group and others can only read:
   ```bash
   umask 022
   ```

3. **Set umask to 077**
   This command sets the umask to `077`, which restricts access so that only the owner can read and write files:
   ```bash
   umask 077
   ```

4. **Display umask in Symbolic Format**
   To view the current umask in symbolic format:
   ```bash
   umask -S
   ```

5. **Set umask Temporarily**
   To set a temporary umask for a single command:
   ```bash
   (umask 007; touch newfile)
   ```

## Tips
- Use `umask` wisely to ensure that sensitive files are not accessible to unauthorized users.
- Remember that the umask value is subtracted from the default permissions, so a lower umask value means more permissions for others.
- You can add your umask settings to your shell's configuration file (like `.bashrc` or `.bash_profile`) to make them persistent across sessions.