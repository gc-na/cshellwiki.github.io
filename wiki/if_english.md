# [Linux] Bash if uso: Conditional execution in scripts

## Overview
The `if` command in Bash is used to evaluate conditional expressions and execute commands based on the result. It allows scripts to make decisions, enabling different paths of execution depending on whether a condition is true or false.

## Usage
The basic syntax of the `if` command is as follows:

```bash
if [ condition ]; then
    # commands to execute if condition is true
else
    # commands to execute if condition is false
fi
```

## Common Options
- `-e`: Checks if a file exists.
- `-d`: Checks if a directory exists.
- `-f`: Checks if a file is a regular file.
- `-z`: Checks if the length of a string is zero.
- `-n`: Checks if the length of a string is non-zero.
- `==`: Compares two strings for equality.
- `!=`: Compares two strings for inequality.

## Common Examples

### Example 1: Check if a file exists
```bash
if [ -e "myfile.txt" ]; then
    echo "File exists."
else
    echo "File does not exist."
fi
```

### Example 2: Check if a directory exists
```bash
if [ -d "/mydirectory" ]; then
    echo "Directory exists."
else
    echo "Directory does not exist."
fi
```

### Example 3: String comparison
```bash
name="Alice"
if [ "$name" == "Alice" ]; then
    echo "Hello, Alice!"
else
    echo "Who are you?"
fi
```

### Example 4: Check if a variable is empty
```bash
var=""
if [ -z "$var" ]; then
    echo "Variable is empty."
else
    echo "Variable is not empty."
fi
```

## Tips
- Always use quotes around variables to prevent errors with spaces or special characters.
- Use `elif` for multiple conditions to avoid deeply nested `if` statements.
- Indent your commands within `if` blocks for better readability.
- Remember to close your `if` statements with `fi` to avoid syntax errors.