# [Linux] Bash else Usage: Conditional execution in scripts

## Overview
The `else` command in Bash is used as part of conditional statements to execute a block of code when the preceding `if` condition evaluates to false. It allows for more complex decision-making in scripts, enabling different actions based on varying conditions.

## Usage
The basic syntax for using `else` in a Bash script is as follows:

```bash
if [ condition ]; then
    # commands if condition is true
else
    # commands if condition is false
fi
```

## Common Options
The `else` command itself does not have options, but it is typically used in conjunction with `if` statements that may include various test conditions. Here are some common conditions you might use with `if`:

- `-e`: Checks if a file exists.
- `-d`: Checks if a directory exists.
- `-f`: Checks if a file is a regular file.
- `-z`: Checks if a string is empty.

## Common Examples

### Example 1: Basic if-else
```bash
if [ -e "file.txt" ]; then
    echo "file.txt exists."
else
    echo "file.txt does not exist."
fi
```

### Example 2: Checking a variable
```bash
name="Alice"
if [ "$name" == "Bob" ]; then
    echo "Hello, Bob!"
else
    echo "Hello, stranger!"
fi
```

### Example 3: Using with numeric comparison
```bash
number=10
if [ $number -gt 5 ]; then
    echo "Number is greater than 5."
else
    echo "Number is 5 or less."
fi
```

### Example 4: Nested if-else
```bash
if [ -f "file.txt" ]; then
    echo "file.txt is a regular file."
else
    if [ -d "file.txt" ]; then
        echo "file.txt is a directory."
    else
        echo "file.txt does not exist."
    fi
fi
```

## Tips
- Always ensure to close your `if` statements with `fi` to avoid syntax errors.
- Use clear and descriptive messages in your `echo` commands to make your scripts easier to understand.
- Consider using `elif` for multiple conditions to avoid deep nesting of `if` statements, which can make the script harder to read.