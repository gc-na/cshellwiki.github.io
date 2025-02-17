# [Linux] Bash fmt utilizare: [formatiranje teksta u datoteci]

## Overview
The `fmt` command is a simple text formatting utility in Bash that helps to format paragraphs of text to a specified width. It is particularly useful for preparing text files for better readability by adjusting line lengths.

## Usage
The basic syntax of the `fmt` command is as follows:

```bash
fmt [options] [arguments]
```

## Common Options
- `-w <width>`: Set the maximum line width for the output (default is 75 characters).
- `-s`: Suppress splitting of long lines; it will keep them as they are.
- `-c`: Use a "c" style formatting, which preserves the indentation of the first line of each paragraph.

## Common Examples
Here are some practical examples of using the `fmt` command:

1. **Basic Formatting**: Format a text file to the default width.
   ```bash
   fmt myfile.txt
   ```

2. **Specify a Custom Width**: Format a text file to a specific width of 50 characters.
   ```bash
   fmt -w 50 myfile.txt
   ```

3. **Suppress Long Line Splitting**: Format a file but keep long lines intact.
   ```bash
   fmt -s myfile.txt
   ```

4. **C Style Formatting**: Format a file while preserving the indentation of the first line.
   ```bash
   fmt -c myfile.txt
   ```

## Tips
- Always check the output of `fmt` with a small sample of text before applying it to larger files to ensure it meets your formatting needs.
- Combine `fmt` with other commands like `cat` or `less` for better text viewing and manipulation.
- Use `man fmt` to explore more options and detailed usage of the command.