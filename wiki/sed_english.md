# [Linux] Bash sed Usage: Stream editor for filtering and transforming text

## Overview
The `sed` command, short for stream editor, is a powerful utility in Unix and Linux environments used for parsing and transforming text from input streams or files. It allows users to perform basic text transformations on an input stream (a file or input from a pipeline) using a simple and compact syntax.

## Usage
The basic syntax of the `sed` command is as follows:

```bash
sed [options] [script] [file...]
```

- **options**: Various flags that modify the behavior of `sed`.
- **script**: The set of commands to be executed.
- **file**: The input file(s) to be processed. If no file is specified, `sed` reads from standard input.

## Common Options
- `-e`: Allows you to add the script to the commands to be executed.
- `-f`: Specifies a file containing `sed` commands to be executed.
- `-i`: Edits files in place (modifies the original file).
- `-n`: Suppresses automatic printing of pattern space; useful when you want to control what gets printed.
- `s/pattern/replacement/`: The substitute command, used to replace occurrences of a pattern with a replacement string.

## Common Examples

### 1. Substitute text in a file
Replace the first occurrence of "apple" with "orange" in a file called `fruits.txt`:

```bash
sed 's/apple/orange/' fruits.txt
```

### 2. Substitute text globally
Replace all occurrences of "apple" with "orange" in `fruits.txt`:

```bash
sed 's/apple/orange/g' fruits.txt
```

### 3. Edit a file in place
Replace "apple" with "orange" directly in `fruits.txt`:

```bash
sed -i 's/apple/orange/g' fruits.txt
```

### 4. Print specific lines
Print only lines 2 to 4 from `fruits.txt`:

```bash
sed -n '2,4p' fruits.txt
```

### 5. Delete lines containing a pattern
Remove all lines containing the word "banana" from `fruits.txt`:

```bash
sed '/banana/d' fruits.txt
```

## Tips
- Always make a backup of your files before using the `-i` option to prevent accidental data loss.
- Use the `-n` option in combination with the `p` command to have more control over what gets printed.
- You can chain multiple `sed` commands using `-e` or by separating them with a semicolon within a single script.
- Regular expressions can be used in `sed` for more complex pattern matching and substitutions.