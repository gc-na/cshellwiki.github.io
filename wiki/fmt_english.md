# [Linux] Bash fmt用法: Format text paragraphs

## Overview
The `fmt` command in Bash is used to format text files by adjusting the line length and ensuring that paragraphs are neatly organized. It helps in making text more readable by wrapping lines to a specified width.

## Usage
The basic syntax of the `fmt` command is as follows:

```bash
fmt [options] [arguments]
```

## Common Options
- `-w, --width=N`: Set the maximum line width to N characters (default is 75).
- `-s, --split-only`: Only split long lines, do not join short ones.
- `-p, --prefix=STRING`: Prefix each output line with the specified string.
- `-c, --crown`: Center the text in the output.

## Common Examples

1. **Basic Formatting**
   Format a text file to the default width of 75 characters:
   ```bash
   fmt myfile.txt
   ```

2. **Setting a Custom Width**
   Format a text file with a maximum line width of 50 characters:
   ```bash
   fmt -w 50 myfile.txt
   ```

3. **Splitting Long Lines Only**
   Split long lines without joining shorter ones:
   ```bash
   fmt -s myfile.txt
   ```

4. **Adding a Prefix**
   Prefix each line of the formatted output with "Note: ":
   ```bash
   fmt -p "Note: " myfile.txt
   ```

5. **Centering Text**
   Center the text in the output:
   ```bash
   fmt -c myfile.txt
   ```

## Tips
- Always check the output of `fmt` with a sample file to ensure it meets your formatting needs.
- Use the `-w` option to customize the line length based on your specific requirements for different documents.
- Consider combining `fmt` with other commands like `cat` or `echo` for more complex text processing tasks.