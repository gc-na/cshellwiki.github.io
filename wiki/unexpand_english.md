# [Linux] Bash unexpand Usage: Convert tabs to spaces in text files

## Overview
The `unexpand` command in Bash is used to convert tabs in a text file into spaces. This is particularly useful when you want to ensure consistent spacing in files, especially for programming or configuration files where tabs may cause formatting issues.

## Usage
The basic syntax of the `unexpand` command is as follows:

```
unexpand [options] [arguments]
```

## Common Options
- `-t, --tabs=N`: Specify the number of spaces per tab. By default, this is set to 8.
- `-a, --all`: Convert all tabs to spaces, regardless of their position.
- `-i, --initial`: Ignore leading tabs when converting.
- `-h, --help`: Display help information about the command.

## Common Examples

1. **Convert tabs to spaces in a file**:
   To convert tabs to spaces in a file named `example.txt` using the default tab size of 8 spaces:
   ```bash
   unexpand example.txt
   ```

2. **Specify a custom tab size**:
   To convert tabs to spaces with a custom tab size of 4 spaces:
   ```bash
   unexpand -t 4 example.txt
   ```

3. **Convert all tabs to spaces**:
   To convert all tabs in a file, regardless of their position:
   ```bash
   unexpand -a example.txt
   ```

4. **Ignore leading tabs**:
   To convert tabs to spaces while ignoring leading tabs:
   ```bash
   unexpand -i example.txt
   ```

5. **Output to a new file**:
   To save the output to a new file instead of displaying it on the terminal:
   ```bash
   unexpand example.txt > output.txt
   ```

## Tips
- Always check the output of `unexpand` with a command like `cat` or `less` to ensure the formatting is as expected.
- Use the `-h` option to quickly access help and see all available options if you're unsure.
- Consider using `unexpand` in combination with other commands like `grep` or `sed` for more complex text processing tasks.