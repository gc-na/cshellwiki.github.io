# [Linux] Bash awk Uso equivalente: Process text files and data

## Overview
The `awk` command is a powerful text processing tool in Bash that allows users to manipulate and analyze data in files or input streams. It is particularly useful for extracting and reporting information from structured text files, such as CSV or tab-delimited files.

## Usage
The basic syntax of the `awk` command is as follows:

```bash
awk [options] 'pattern { action }' file
```

- `pattern`: A condition to match lines in the input.
- `action`: The operation to perform on the matched lines.
- `file`: The input file to process.

## Common Options
- `-F`: Specify the field separator (default is whitespace).
- `-v`: Assign a value to a variable before execution.
- `-f`: Read the `awk` program from a file instead of the command line.
- `-W`: Enable specific features or warnings.

## Common Examples

### Example 1: Print specific columns
To print the first and third columns of a file:

```bash
awk '{print $1, $3}' filename.txt
```

### Example 2: Using a custom field separator
If your file is comma-separated, you can specify the separator with the `-F` option:

```bash
awk -F, '{print $1, $2}' filename.csv
```

### Example 3: Filtering lines
To print only the lines where the second column is greater than 100:

```bash
awk '$2 > 100' filename.txt
```

### Example 4: Counting lines
To count the number of lines in a file:

```bash
awk 'END {print NR}' filename.txt
```

### Example 5: Using variables
You can use the `-v` option to set a variable and use it in your `awk` command:

```bash
awk -v threshold=50 '$1 > threshold' filename.txt
```

## Tips
- Always quote your `awk` commands to prevent shell interpretation of special characters.
- Use the `-F` option to handle different delimiters effectively.
- Combine `awk` with other commands using pipes for more complex data processing tasks.
- Familiarize yourself with regular expressions to enhance your pattern matching capabilities in `awk`.