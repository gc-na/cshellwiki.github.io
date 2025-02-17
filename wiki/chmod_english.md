# [Linux] Bash chmod kullanım: Change file permissions

## Overview
The `chmod` command in Bash is used to change the file system permissions of files and directories. It allows users to define who can read, write, or execute a file, thereby controlling access to the file system.

## Usage
The basic syntax of the `chmod` command is as follows:

```bash
chmod [options] [permissions] [file]
```

## Common Options
- `-R`: Recursively change permissions for directories and their contents.
- `-v`: Verbosely show the changes made.
- `-c`: Report only when a change is made.
- `--reference=RFILE`: Use the permissions of RFILE instead of specifying them explicitly.

## Common Examples

1. **Change permissions to read and write for the owner, and read for group and others:**
   ```bash
   chmod 644 filename.txt
   ```

2. **Add execute permission for the owner:**
   ```bash
   chmod u+x script.sh
   ```

3. **Remove write permission for group:**
   ```bash
   chmod g-w document.pdf
   ```

4. **Recursively change permissions to read, write, and execute for everyone in a directory:**
   ```bash
   chmod -R 777 /path/to/directory
   ```

5. **Set permissions using symbolic notation to give read and execute permissions to everyone:**
   ```bash
   chmod a+rx program
   ```

## Tips
- Always double-check permissions before applying changes, especially with the `-R` option, to avoid unintended access.
- Use the `-v` or `-c` options to keep track of changes made, especially in scripts.
- Be cautious with `777` permissions as it allows everyone full access, which can pose security risks.