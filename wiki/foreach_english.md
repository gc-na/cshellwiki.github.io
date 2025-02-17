# [Linux] Bash foreach Usage: Iterate over a list of items

## Overview
The `foreach` command is a loop construct used in some shell environments, notably in C shell (csh) and its derivatives, to iterate over a list of items. However, in Bash, the equivalent functionality is achieved using the `for` loop. This allows users to execute a set of commands for each item in a list.

## Usage
The basic syntax for the `for` loop in Bash is as follows:

```bash
for variable in list; do
    commands
done
```

## Common Options
While the `for` loop itself does not have options like other commands, you can use various constructs within the loop to control its behavior:

- `in`: Specifies the list of items to iterate over.
- `do`: Begins the block of commands to execute for each item.
- `done`: Ends the loop block.

## Common Examples

### Example 1: Simple Iteration
This example demonstrates a basic iteration over a list of numbers.

```bash
for i in 1 2 3 4 5; do
    echo "Number: $i"
done
```

### Example 2: Iterating Over Files
You can use the `for` loop to iterate over files in a directory.

```bash
for file in *.txt; do
    echo "Processing file: $file"
done
```

### Example 3: Using a C-style for loop
Bash also supports a C-style syntax for loops.

```bash
for ((i = 0; i < 5; i++)); do
    echo "Count: $i"
done
```

### Example 4: Reading Lines from a File
This example shows how to read lines from a file and process each line.

```bash
for line in $(cat myfile.txt); do
    echo "Line: $line"
done
```

## Tips
- Always quote variables (e.g., `"$file"`) to prevent issues with filenames containing spaces.
- Use `$(...)` for command substitution instead of backticks for better readability and nesting.
- Consider using `while` loops for more complex conditions or when reading from files, as they can provide more control over the input.

By utilizing the `for` loop in Bash, you can efficiently handle repetitive tasks and automate processes in your scripts.