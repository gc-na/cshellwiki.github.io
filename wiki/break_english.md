# [Linux] Bash break Usage: Exit from loops

## Overview
The `break` command in Bash is used to exit from a loop prematurely. It allows you to terminate the execution of a loop when a certain condition is met, which can be particularly useful in controlling the flow of your scripts.

## Usage
The basic syntax of the `break` command is as follows:

```bash
break [n]
```

Here, `n` is an optional argument that specifies how many levels of enclosing loops to break out of. If `n` is not provided, it defaults to 1, meaning it will exit the innermost loop.

## Common Options
- `n`: An optional integer that specifies the number of nested loops to exit. If omitted, it exits the innermost loop.

## Common Examples

### Example 1: Basic Loop Exit
This example demonstrates a simple loop that exits when a specific condition is met.

```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo "Number: $i"
done
```
**Output:**
```
Number: 1
Number: 2
```

### Example 2: Exiting Nested Loops
In this example, we use `break` with an argument to exit from a nested loop.

```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      break 2
    fi
    echo "i: $i, j: $j"
  done
done
```
**Output:**
```
i: 1, j: 1
```

### Example 3: Using break in a While Loop
Here’s how to use `break` in a `while` loop.

```bash
count=1
while true; do
  if [ $count -gt 5 ]; then
    break
  fi
  echo "Count: $count"
  ((count++))
done
```
**Output:**
```
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
```

## Tips
- Use `break` to improve the efficiency of your scripts by avoiding unnecessary iterations.
- Always ensure that your break conditions are clearly defined to prevent infinite loops.
- Consider using `break` in combination with `continue` to manage loop control more effectively.