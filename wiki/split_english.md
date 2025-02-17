# [Linux] Bash split uso: Divide files into smaller pieces

## Overview
The `split` command in Bash is used to divide a large file into smaller, more manageable pieces. This can be particularly useful for processing large datasets or for transferring files that exceed size limits.

## Usage
The basic syntax of the `split` command is as follows:

```bash
split [options] [arguments]
```

## Common Options
- `-l NUM`: Split the file into pieces with a specified number of lines (NUM).
- `-b SIZE`: Split the file into pieces of a specified size (SIZE), which can include suffixes like `k` for kilobytes or `m` for megabytes.
- `-d`: Use numeric suffixes instead of alphabetic for the output files.
- `--additional-suffix=SUFFIX`: Append a specified suffix to the output files.

## Common Examples

### Split by Number of Lines
To split a file into pieces of 100 lines each:

```bash
split -l 100 myfile.txt
```

### Split by File Size
To split a file into pieces of 1 megabyte each:

```bash
split -b 1m mylargefile.dat
```

### Use Numeric Suffixes
To split a file and use numeric suffixes for the output files:

```bash
split -d -l 50 myfile.txt
```

### Custom Suffix
To split a file and add a custom suffix to the output files:

```bash
split --additional-suffix=.part -l 20 myfile.txt output_prefix_
```

## Tips
- Always check the output files to ensure they have been split as expected.
- Use the `-n` option to specify the number of output files you want, which can be helpful for evenly distributing data.
- When working with binary files, be cautious as splitting may corrupt the file if not handled properly.