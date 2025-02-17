# [English] Bash nl Usage equivalent in English: Number lines in text files

## Overview
The `nl` command in Bash is used to number the lines of files. It can be particularly useful for adding line numbers to text files for better readability or for processing data in scripts.

## Usage
The basic syntax of the `nl` command is as follows:

```bash
nl [options] [arguments]
```

## Common Options
- `-b` : Specify how to number lines. Options include `a` (number all lines), `t` (number only non-empty lines), and `p` (number lines based on a regular expression).
- `-f` : Specify the number of lines to be skipped before numbering.
- `-h` : Specify a header to be printed before the numbered lines.
- `-n` : Control the format of the line numbers. Options include `ln` (left justified), `rn` (right justified), and `zn` (zero-padded).
- `-w` : Specify the width of the line numbers.

## Common Examples

### Example 1: Basic Line Numbering
To number all lines in a text file called `example.txt`, you can use:

```bash
nl example.txt
```

### Example 2: Numbering Only Non-Empty Lines
To number only the non-empty lines in `example.txt`, use the `-b t` option:

```bash
nl -b t example.txt
```

### Example 3: Customizing Line Number Format
To number lines with right justification and a width of 5, you can use:

```bash
nl -n rn -w 5 example.txt
```

### Example 4: Adding a Header
To add a header before the numbered lines, use the `-h` option:

```bash
nl -h "Header: Line Numbers" example.txt
```

### Example 5: Skipping Lines
To skip the first 2 lines of `example.txt` before numbering, use the `-f` option:

```bash
nl -f 2 example.txt
```

## Tips
- Use `nl` in combination with other commands in a pipeline for more complex processing of text files.
- Always check the output format with different options to ensure it meets your needs.
- Consider redirecting the output to a new file if you want to save the numbered lines:

```bash
nl example.txt > numbered_example.txt
```