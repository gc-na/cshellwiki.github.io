# [Linux] Bash while loop: Execute commands repeatedly

## Overview
The `while` command in Bash is used to create a loop that continues to execute a set of commands as long as a specified condition evaluates to true. This is particularly useful for automating repetitive tasks or processing data until a certain condition is met.

## Usage
The basic syntax of the `while` command is as follows:

```bash
while [ condition ]; do
    # commands to be executed
done
```

## Common Options
The `while` command itself does not have specific options, but the condition can involve various test commands or expressions, such as:
- `-e`: Check if a file exists.
- `-z`: Check if a string is empty.
- `-gt`: Check if one number is greater than another.

## Common Examples

### Example 1: Counting from 1 to 5
This example demonstrates a simple loop that counts from 1 to 5.

```bash
count=1
while [ $count -le 5 ]; do
    echo "Count is: $count"
    ((count++))
done
```

### Example 2: Reading lines from a file
This example reads each line from a file and prints it.

```bash
filename="example.txt"
while IFS= read -r line; do
    echo "$line"
done < "$filename"
```

### Example 3: Infinite loop with break condition
This example creates an infinite loop that breaks when a specific condition is met.

```bash
while true; do
    read -p "Enter 'exit' to quit: " input
    if [ "$input" == "exit" ]; then
        echo "Exiting the loop."
        break
    fi
done
```

## Tips
- Always ensure that the condition in the `while` loop will eventually become false to avoid infinite loops.
- Use `break` to exit the loop prematurely when needed.
- Consider using `sleep` within the loop to prevent high CPU usage if the loop runs frequently. For example, `sleep 1` will pause the loop for 1 second on each iteration.