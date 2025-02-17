# [Linux] Bash tee uso equivalente: Redirect output to files and display it

## Overview
The `tee` command in Bash is used to read from standard input and write to standard output and files simultaneously. This allows users to view the output of a command while also saving it to a file.

## Usage
The basic syntax of the `tee` command is as follows:

```bash
tee [options] [arguments]
```

## Common Options
- `-a`, `--append`: Append the output to the specified files instead of overwriting them.
- `-i`, `--ignore-interrupts`: Ignore interrupt signals.
- `-p`, `--output-error`: Control the behavior when writing to the output file fails.

## Common Examples

### Example 1: Basic usage
To display the output of a command and save it to a file:
```bash
echo "Hello, World!" | tee output.txt
```
This command will print "Hello, World!" to the terminal and save it to `output.txt`.

### Example 2: Appending to a file
To append output to an existing file:
```bash
echo "Another line" | tee -a output.txt
```
This will add "Another line" to the end of `output.txt` without removing the previous content.

### Example 3: Using with multiple files
To write output to multiple files:
```bash
echo "Data saved" | tee file1.txt file2.txt
```
This command will save "Data saved" to both `file1.txt` and `file2.txt`.

### Example 4: Redirecting error output
To redirect both standard output and error output to a file:
```bash
command 2>&1 | tee output.txt
```
Replace `command` with any command you want to run. This will capture both the output and any errors in `output.txt`.

## Tips
- Use `tee` in combination with other commands in a pipeline to monitor and log outputs simultaneously.
- Always check the contents of your output files after using `tee` to ensure data was written as expected.
- When using `tee` with `sudo`, be cautious as it can overwrite files with elevated permissions.