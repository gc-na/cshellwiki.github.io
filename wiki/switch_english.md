# [Linux] Bash switch usage: Switch between options

## Overview
The `switch` command in Bash is not a standard command; however, it is often used in the context of conditional statements within scripts. It allows users to execute different blocks of code based on the value of a variable. This is particularly useful for handling multiple conditions in a clean and organized manner.

## Usage
The basic syntax for using a switch statement in a Bash script is as follows:

```bash
case [variable] in
    [pattern1])
        # commands for pattern1
        ;;
    [pattern2])
        # commands for pattern2
        ;;
    *)
        # commands for default case
        ;;
esac
```

## Common Options
While `switch` itself does not have options like traditional commands, the `case` statement can handle various patterns and conditions. Here are some common patterns you might use:

- `*` - Matches any value (default case).
- `?` - Matches any single character.
- `[abc]` - Matches any single character within the brackets.
- `[a-z]` - Matches any single character in the specified range.

## Common Examples

### Example 1: Basic Case Statement
```bash
#!/bin/bash
read -p "Enter a number (1-3): " num

case $num in
    1)
        echo "You selected one."
        ;;
    2)
        echo "You selected two."
        ;;
    3)
        echo "You selected three."
        ;;
    *)
        echo "Invalid selection."
        ;;
esac
```

### Example 2: File Type Check
```bash
#!/bin/bash
file="example.txt"

case $file in
    *.txt)
        echo "This is a text file."
        ;;
    *.jpg|*.png)
        echo "This is an image file."
        ;;
    *)
        echo "Unknown file type."
        ;;
esac
```

### Example 3: Day of the Week
```bash
#!/bin/bash
day=$(date +%A)

case $day in
    Monday)
        echo "Start of the work week."
        ;;
    Friday)
        echo "Almost the weekend!"
        ;;
    Saturday|Sunday)
        echo "It's the weekend!"
        ;;
    *)
        echo "Midweek days."
        ;;
esac
```

## Tips
- Always include a default case (`*`) to handle unexpected values.
- Use clear and descriptive patterns to make your code more readable.
- Consider using `[[` for more complex conditions when necessary.
- Keep your case statements organized to improve maintainability.