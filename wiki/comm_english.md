# [Linux] Bash comm comando: compare sorted files line by line

## Overview
The `comm` command in Bash is used to compare two sorted files line by line. It outputs the lines that are unique to each file and the lines that are common to both. This command is particularly useful for identifying differences and similarities between two datasets.

## Usage
The basic syntax of the `comm` command is as follows:

```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`: Suppress the output of lines unique to the first file.
- `-2`: Suppress the output of lines unique to the second file.
- `-3`: Suppress the output of lines that are common to both files.
- `--nocheck-order`: Do not check if the input files are sorted.
- `-i`: Ignore case differences when comparing lines.

## Common Examples

### Example 1: Basic Comparison
To compare two sorted files, `file1.txt` and `file2.txt`, and display all unique and common lines:

```bash
comm file1.txt file2.txt
```

### Example 2: Suppress Unique Lines from First File
To display only the lines that are common to both files and the unique lines from the second file:

```bash
comm -2 file1.txt file2.txt
```

### Example 3: Suppress Common Lines
To show only the lines unique to the first file:

```bash
comm -13 file1.txt file2.txt
```

### Example 4: Ignore Case Differences
To compare two files while ignoring case sensitivity:

```bash
comm -i file1.txt file2.txt
```

## Tips
- Ensure that both files are sorted before using `comm`, as it requires sorted input for accurate comparisons.
- Use the `sort` command to sort files if they are not already sorted, e.g., `sort file1.txt > sorted_file1.txt`.
- Combine `comm` with other commands using pipes for more complex data processing tasks.