# [Linux] Bash iconv Uso: Convert character encoding

## Overview
The `iconv` command is a powerful utility in Unix-like systems that allows users to convert text from one character encoding to another. This is particularly useful when dealing with files that may not be compatible with the current system's encoding.

## Usage
The basic syntax of the `iconv` command is as follows:

```bash
iconv [options] [arguments]
```

## Common Options
- `-f, --from-code=CODE`: Specify the encoding of the input text.
- `-t, --to-code=CODE`: Specify the encoding for the output text.
- `-o, --output=FILE`: Write the output to a specified file instead of standard output.
- `-c`: Ignore invalid characters in the input.
- `-l, --list`: List all available encodings.

## Common Examples

1. **Convert a file from UTF-8 to ISO-8859-1:**
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. **Convert a file and display the output in the terminal:**
   ```bash
   iconv -f UTF-8 -t UTF-16 input.txt
   ```

3. **Convert a file while ignoring invalid characters:**
   ```bash
   iconv -f UTF-8 -t ASCII//TRANSLIT -c input.txt -o output.txt
   ```

4. **List all available encodings:**
   ```bash
   iconv -l
   ```

## Tips
- Always check the current encoding of your files before conversion to avoid data loss.
- Use the `-o` option to save the converted output to a new file, preserving the original file.
- When converting to ASCII, consider using `//TRANSLIT` to approximate characters that cannot be represented in ASCII.