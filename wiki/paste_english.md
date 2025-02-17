# [Linux] Bash paste Usage: Combine lines of files

## Overview
The `paste` command in Bash is used to merge lines of files side by side. It takes input from one or more files and concatenates corresponding lines, allowing for easy comparison or combination of data.

## Usage
The basic syntax of the `paste` command is as follows:

```bash
paste [options] [arguments]
```

## Common Options
- `-d`: Specify a delimiter to use between the pasted lines instead of the default tab.
- `-s`: Paste the lines of each file sequentially rather than in parallel.
- `-z`: Treat input lines as null-terminated instead of newline-terminated.

## Common Examples

### Example 1: Basic Usage
To paste two files side by side using the default tab delimiter:

```bash
paste file1.txt file2.txt
```

### Example 2: Using a Custom Delimiter
To use a comma as a delimiter instead of the default tab:

```bash
paste -d, file1.txt file2.txt
```

### Example 3: Sequential Pasting
To paste the contents of a single file sequentially:

```bash
paste -s file1.txt
```

### Example 4: Pasting Multiple Files
To paste multiple files together:

```bash
paste file1.txt file2.txt file3.txt
```

### Example 5: Null-terminated Input
To paste files that use null characters as line terminators:

```bash
paste -z file1.txt file2.txt
```

## Tips
- When using custom delimiters, ensure that the chosen character does not appear in the data to avoid confusion.
- The `-s` option can be particularly useful when you want to create a single line from multiple lines in a file.
- Remember that `paste` will only combine lines up to the length of the shortest file; any extra lines in longer files will be ignored.