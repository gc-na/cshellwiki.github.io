# [Linux] Bash od usage: Display file contents in various formats

## Overview
The `od` command, short for "octal dump," is a utility in Unix-like operating systems that allows users to view the contents of files in various formats, such as octal, hexadecimal, and ASCII. It is particularly useful for examining binary files or understanding the underlying data structure of files.

## Usage
The basic syntax of the `od` command is as follows:

```bash
od [options] [arguments]
```

## Common Options
- `-A, --address-radix=RADIX`: Specifies the base for the output address. Options include `d` for decimal, `o` for octal, `x` for hexadecimal, and `n` for none.
- `-t, --output-format=TYPE`: Defines the output format. Common types include `o` (octal), `x` (hexadecimal), `d` (decimal), `c` (ASCII characters), and `s` (string).
- `-N, --read-bytes=N`: Limits the number of bytes to read from the input file.
- `-v, --output-duplicates`: Shows all output, including duplicate lines.

## Common Examples
Here are several practical examples of using the `od` command:

1. **Display the contents of a file in octal format:**
   ```bash
   od -c filename.txt
   ```

2. **View a binary file in hexadecimal format:**
   ```bash
   od -x binaryfile.bin
   ```

3. **Show the first 16 bytes of a file in decimal format:**
   ```bash
   od -N 16 -d filename.txt
   ```

4. **Display the contents of a file with addresses in hexadecimal:**
   ```bash
   od -A x -t x1 filename.txt
   ```

5. **Output all duplicates when viewing a file:**
   ```bash
   od -v -t c filename.txt
   ```

## Tips
- Use the `-A` option to change how addresses are displayed, which can help in debugging or analyzing binary data.
- Combine multiple options to customize the output format to your needs, such as using `-t` with `-N` to limit the output to a specific format and byte count.
- When working with large files, consider using `head` or `tail` in conjunction with `od` to limit the amount of data you are examining at once.