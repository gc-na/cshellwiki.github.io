# [Linux] Bash mkdir Uso equivalente: Create directories

## Overview
The `mkdir` command in Bash is used to create new directories in the filesystem. It allows users to organize files and manage their directory structure efficiently.

## Usage
The basic syntax of the `mkdir` command is as follows:

```bash
mkdir [options] [arguments]
```

## Common Options
- `-p`: Create parent directories as needed. If the specified directory path does not exist, it will create all necessary parent directories.
- `-v`: Verbose mode. It will display a message for each created directory.
- `-m`: Set the file mode (permissions) for the new directory.

## Common Examples
Here are some practical examples of using the `mkdir` command:

1. **Create a single directory:**
   ```bash
   mkdir my_directory
   ```

2. **Create multiple directories at once:**
   ```bash
   mkdir dir1 dir2 dir3
   ```

3. **Create a directory with parent directories:**
   ```bash
   mkdir -p parent_dir/child_dir
   ```

4. **Create a directory and set permissions:**
   ```bash
   mkdir -m 755 my_secure_directory
   ```

5. **Create directories and see the output:**
   ```bash
   mkdir -v new_directory
   ```

## Tips
- Always use the `-p` option when creating nested directories to avoid errors if the parent directories do not exist.
- Use the `-v` option for confirmation that your directories have been created, especially when running scripts.
- Consider setting appropriate permissions with the `-m` option to ensure the right access levels for your directories.