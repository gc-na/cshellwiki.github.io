# [Linux] Bash rev: Reverse lines of text

## Overview
The `rev` command in Bash is used to reverse the characters of each line in a given input. This can be useful for various text processing tasks, such as manipulating strings or preparing data for specific formats.

## Usage
The basic syntax of the `rev` command is as follows:

```bash
rev [options] [arguments]
```

## Common Options
- `-h`, `--help`: Displays help information about the command.
- `-V`, `--version`: Shows the version of the `rev` command.

## Common Examples

### Example 1: Reverse a simple string
To reverse the characters of a string, you can echo the string and pipe it to `rev`:

```bash
echo "Hello, World!" | rev
```
**Output:**
```
!dlroW ,olleH
```

### Example 2: Reverse lines in a file
If you have a text file named `example.txt`, you can reverse the lines in the file like this:

```bash
rev example.txt
```
**Output:**
```
!dlroW ,olleH
!ereht ,olleH
```

### Example 3: Reverse multiple lines
You can also reverse multiple lines of text directly from the command line:

```bash
printf "Line 1\nLine 2\nLine 3\n" | rev
```
**Output:**
```
1 eniL
2 eniL
3 eniL
```

## Tips
- Use `rev` in combination with other commands for more complex text processing, such as using `cat` to read from multiple files.
- Remember that `rev` processes each line independently, so the output will maintain the original line structure.
- If you want to save the reversed output to a new file, you can redirect the output like this:

```bash
rev example.txt > reversed.txt
```