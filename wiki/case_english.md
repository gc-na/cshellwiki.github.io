# [Linux] Bash case usage: Conditional pattern matching

## Overview
The `case` command in Bash is used for conditional pattern matching. It allows you to execute different blocks of code based on the value of a variable, making it a powerful tool for handling multiple conditions in shell scripts.

## Usage
The basic syntax of the `case` command is as follows:

```bash
case [variable] in
    [pattern1])
        # commands for pattern1
        ;;
    [pattern2])
        # commands for pattern2
        ;;
    *)
        # commands if no patterns match
        ;;
esac
```

## Common Options
The `case` command does not have many options like other commands, but here are some key points to remember:
- Patterns can include wildcards (`*`, `?`) to match multiple values.
- The `*)` pattern acts as a default case, similar to an `else` statement.

## Common Examples

### Example 1: Simple case statement
```bash
fruit="apple"

case $fruit in
    apple)
        echo "This is an apple."
        ;;
    banana)
        echo "This is a banana."
        ;;
    *)
        echo "Unknown fruit."
        ;;
esac
```

### Example 2: Using wildcards
```bash
file="report_2023.txt"

case $file in
    *.txt)
        echo "This is a text file."
        ;;
    *.pdf)
        echo "This is a PDF file."
        ;;
    *)
        echo "Unknown file type."
        ;;
esac
```

### Example 3: Multiple patterns
```bash
color="red"

case $color in
    red|blue|green)
        echo "This is a primary color."
        ;;
    yellow)
        echo "This is a secondary color."
        ;;
    *)
        echo "Unknown color."
        ;;
esac
```

## Tips
- Always end each command block with `;;` to indicate the end of that case.
- Use the `*)` pattern to handle unexpected or default cases.
- Keep your patterns organized to improve readability, especially when handling multiple conditions.