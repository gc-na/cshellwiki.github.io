# [Linux] Bash sort uso: Sorts lines of text files

## Overview
The `sort` command in Bash is used to arrange the lines of text files in a specified order. By default, it sorts lines alphabetically, but it can also sort numerically or based on specific fields, making it a versatile tool for data manipulation.

## Usage
The basic syntax of the `sort` command is as follows:

```bash
sort [options] [arguments]
```

## Common Options
- `-n`: Sorts lines numerically.
- `-r`: Reverses the sort order (descending).
- `-k`: Specifies a key (or field) to sort by.
- `-u`: Outputs only the first of an equal run (removes duplicates).
- `-o`: Writes the output to a specified file instead of standard output.

## Common Examples

### Example 1: Basic Alphabetical Sort
To sort a text file named `file.txt` alphabetically:

```bash
sort file.txt
```

### Example 2: Numeric Sort
To sort a file containing numbers, `numbers.txt`, numerically:

```bash
sort -n numbers.txt
```

### Example 3: Reverse Sort
To sort a file in reverse order:

```bash
sort -r file.txt
```

### Example 4: Sort by Specific Field
To sort a file based on the second column (field) of a space-separated file, `data.txt`:

```bash
sort -k 2 data.txt
```

### Example 5: Remove Duplicates
To sort a file and remove duplicate lines:

```bash
sort -u file.txt
```

### Example 6: Output to a New File
To sort a file and save the output to a new file called `sorted.txt`:

```bash
sort -o sorted.txt file.txt
```

## Tips
- Always check the contents of your files before sorting to ensure the desired order.
- Use the `-k` option to sort by specific fields, especially in structured data like CSV files.
- Combine `sort` with other commands using pipes for more complex data processing tasks. For example, you can use `cat` and `sort` together: `cat file.txt | sort`.
- Consider using `-t` to specify a delimiter when sorting files with different field separators.