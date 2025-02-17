# [Linux] Bash cksum Usage: Calculate file checksums

## Overview
The `cksum` command in Bash is used to compute and display the checksum (a unique identifier) of a file along with its byte size. This is useful for verifying the integrity of files by ensuring that they have not been altered.

## Usage
The basic syntax of the `cksum` command is as follows:

```bash
cksum [options] [arguments]
```

## Common Options
- `-a, --algorithm=ALGO`: Specify the checksum algorithm to use (e.g., `md5`, `sha256`).
- `-h, --help`: Display help information about the command.
- `-V, --version`: Show version information of the `cksum` command.

## Common Examples

1. **Calculate the checksum of a single file:**

   ```bash
   cksum myfile.txt
   ```

   This command will output the checksum, byte size, and file name of `myfile.txt`.

2. **Calculate the checksum of multiple files:**

   ```bash
   cksum file1.txt file2.txt
   ```

   This will display the checksums and sizes for both `file1.txt` and `file2.txt`.

3. **Using an algorithm to calculate checksum:**

   ```bash
   cksum -a md5 myfile.txt
   ```

   This command calculates the MD5 checksum of `myfile.txt`.

4. **Display help information:**

   ```bash
   cksum --help
   ```

   This will show the usage and options available for the `cksum` command.

## Tips
- Always verify the checksum after transferring files to ensure they remain unaltered.
- Use the `-a` option to choose a specific algorithm if you need a particular type of checksum.
- For large files, consider using `cksum` in combination with other commands like `find` to process multiple files efficiently.