# [Linux] Bash printf用法: Format and print data

## Overview
The `printf` command in Bash is used to format and print data to the standard output. It allows for more control over the output format compared to the `echo` command, making it useful for displaying text, numbers, and other data types in a structured way.

## Usage
The basic syntax of the `printf` command is as follows:

```bash
printf [options] format_string [arguments...]
```

## Common Options
- `-v var`: Assign the output to a variable instead of printing it.
- `--help`: Display help information about the command.
- `--version`: Show the version information of the command.

## Common Examples

### Example 1: Basic String Formatting
Print a simple string with a newline.

```bash
printf "Hello, World!\n"
```

### Example 2: Formatting Numbers
Print an integer with leading zeros.

```bash
printf "Number: %05d\n" 42
```

### Example 3: Floating Point Numbers
Print a floating-point number with specified decimal places.

```bash
printf "Pi: %.2f\n" 3.14159
```

### Example 4: Multiple Arguments
Print multiple formatted values in one line.

```bash
printf "Name: %s, Age: %d\n" "Alice" 30
```

### Example 5: Assigning Output to a Variable
Store formatted output in a variable.

```bash
output=$(printf "Formatted Output: %.1f\n" 3.14)
echo "$output"
```

## Tips
- Use `\n` to add new lines in your output.
- Use format specifiers like `%s` for strings, `%d` for integers, and `%f` for floating-point numbers to control how data is displayed.
- Remember that `printf` does not automatically add a newline at the end of the output, so include `\n` if needed.