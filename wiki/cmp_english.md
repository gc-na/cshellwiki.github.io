# [Linux] Bash cmp Usage Equivalent: Compare two files byte by byte

## Overview
The `cmp` command in Bash is used to compare two files byte by byte. It is particularly useful for identifying differences between files, especially binary files, and can help in verifying the integrity of files.

## Usage
The basic syntax of the `cmp` command is as follows:

```bash
cmp [options] [file1] [file2]
```

## Common Options
- `-l`: Print the differing bytes in octal.
- `-s`: Suppress all output; only return the exit status.
- `-i`: Compare only the first `n` bytes.
- `-b`: Print differing bytes in hexadecimal.
- `-h`: Display help information.

## Common Examples

1. **Basic Comparison**
   To compare two text files:
   ```bash
   cmp file1.txt file2.txt
   ```

2. **Suppress Output**
   To check if two files are identical without any output:
   ```bash
   cmp -s file1.txt file2.txt
   ```

3. **Show Differences in Octal**
   To display the differing bytes in octal format:
   ```bash
   cmp -l file1.bin file2.bin
   ```

4. **Compare First N Bytes**
   To compare only the first 10 bytes of two files:
   ```bash
   cmp -i 10 file1.txt file2.txt
   ```

5. **Display Differences in Hexadecimal**
   To print the differing bytes in hexadecimal:
   ```bash
   cmp -b file1.bin file2.bin
   ```

## Tips
- Use `cmp -s` for scripts where you only need to know if files differ without cluttering the output.
- For large binary files, consider using `cmp -l` to get a detailed report of differences without overwhelming output.
- Remember that `cmp` stops comparing at the first difference it finds, which can be useful for quickly identifying discrepancies.