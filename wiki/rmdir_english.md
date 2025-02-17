# [Linux] Bash rmdir uso equivalente: Remove empty directories

## Overview
The `rmdir` command in Bash is used to remove empty directories from the filesystem. It is a straightforward command that helps users clean up their directory structure by deleting directories that no longer contain any files or subdirectories.

## Usage
The basic syntax of the `rmdir` command is as follows:

```bash
rmdir [options] [arguments]
```

## Common Options
- `-p`, `--parents`: Remove empty parent directories as well, if they become empty after the removal of the specified directory.
- `--ignore-fail-on-non-empty`: Do not report an error if the directory is not empty.
- `--verbose`: Provide detailed output about the directories being removed.

## Common Examples

1. **Remove a single empty directory:**
   ```bash
   rmdir my_empty_directory
   ```

2. **Remove multiple empty directories at once:**
   ```bash
   rmdir dir1 dir2 dir3
   ```

3. **Remove an empty directory and its empty parent directory:**
   ```bash
   rmdir -p parent_directory/child_directory
   ```

4. **Verbose output while removing a directory:**
   ```bash
   rmdir --verbose my_empty_directory
   ```

5. **Ignore non-empty directories (no error reported):**
   ```bash
   rmdir --ignore-fail-on-non-empty my_non_empty_directory
   ```

## Tips
- Always ensure that the directory is empty before using `rmdir`, as it will not remove directories that contain files or other directories.
- Use the `-p` option cautiously, as it will remove parent directories if they become empty after the specified directory is removed.
- Consider using `rm -r` if you need to remove non-empty directories, but be aware that this command is more destructive and should be used with caution.