# [Linux] Bash diff uso equivalente: Compare files line by line

## Overview
The `diff` command is a powerful utility in Unix-like operating systems that allows users to compare two files line by line. It identifies the differences between the files and displays them in a format that makes it easy to see what has changed.

## Usage
The basic syntax of the `diff` command is as follows:

```bash
diff [options] [file1] [file2]
```

## Common Options
- `-u`: Outputs the differences in a unified format, which is easier to read.
- `-c`: Produces a context diff, showing a few lines of context around the changes.
- `-i`: Ignores case differences in the file contents.
- `-w`: Ignores all whitespace when comparing lines.
- `-r`: Recursively compares any subdirectories found.

## Common Examples
Here are some practical examples of using the `diff` command:

### Example 1: Basic Comparison
To compare two text files and see the differences:
```bash
diff file1.txt file2.txt
```

### Example 2: Unified Format
To view the differences in a unified format:
```bash
diff -u file1.txt file2.txt
```

### Example 3: Context Diff
To see the differences with context:
```bash
diff -c file1.txt file2.txt
```

### Example 4: Ignoring Case
To compare two files while ignoring case differences:
```bash
diff -i file1.txt file2.txt
```

### Example 5: Comparing Directories
To compare two directories recursively:
```bash
diff -r dir1/ dir2/
```

## Tips
- Use the `-u` option for a more readable output, especially when reviewing changes in code.
- When working with large files, consider using `less` to paginate the output: `diff file1.txt file2.txt | less`.
- Combine `diff` with `patch` to apply changes from one file to another based on the differences identified.