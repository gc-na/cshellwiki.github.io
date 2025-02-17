# [Linux] Bash unxz Usage: Decompress .xz files

## Overview
The `unxz` command is used to decompress files that have been compressed using the XZ compression algorithm. This command is particularly useful for handling `.xz` files, which are commonly used for distributing software packages and data.

## Usage
The basic syntax of the `unxz` command is as follows:

```bash
unxz [options] [arguments]
```

## Common Options
- `-k`, `--keep`: Keep the original `.xz` file after decompression.
- `-f`, `--force`: Force overwrite of output files without prompting.
- `-v`, `--verbose`: Provide detailed output during the decompression process.
- `-h`, `--help`: Display help information about the command and its options.

## Common Examples
Here are some practical examples of using the `unxz` command:

1. **Decompress a single file:**
   ```bash
   unxz file.xz
   ```
   This command will decompress `file.xz` and remove the original file.

2. **Decompress a file and keep the original:**
   ```bash
   unxz -k file.xz
   ```
   This will decompress `file.xz` while keeping the original `.xz` file intact.

3. **Force decompression, overwriting existing files:**
   ```bash
   unxz -f file.xz
   ```
   This command will decompress `file.xz`, overwriting any existing files with the same name.

4. **Verbose output during decompression:**
   ```bash
   unxz -v file.xz
   ```
   This will provide detailed information about the decompression process.

## Tips
- Always check the contents of a `.xz` file before decompression to avoid overwriting important files.
- Use the `-k` option if you want to keep the original compressed file for backup purposes.
- If you frequently work with `.xz` files, consider creating an alias for `unxz` to streamline your workflow.