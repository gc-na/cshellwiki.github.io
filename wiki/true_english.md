# [Linux] Bash true用法: Always returns a successful exit status

## Overview
The `true` command in Bash is a simple utility that does nothing and always returns a successful exit status (0). It is often used in scripts and command lines to indicate success or to serve as a placeholder where a command is required syntactically but no action is desired.

## Usage
The basic syntax of the `true` command is straightforward:

```bash
true [options]
```

Since `true` does not take any arguments or options, it can be invoked simply as `true`.

## Common Options
The `true` command does not have any options or arguments. It is designed to be as minimal as possible, serving its purpose without additional complexity.

## Common Examples

### Example 1: Basic Usage
Simply running the command will return a success status:
```bash
true
```

### Example 2: Using true in Conditional Statements
You can use `true` in conditional statements to create loops or checks that always succeed:
```bash
while true; do
    echo "This will run indefinitely."
done
```

### Example 3: Placeholder in Scripts
You can use `true` as a placeholder in scripts where a command is syntactically required:
```bash
if some_condition; then
    true
else
    echo "Condition not met."
fi
```

### Example 4: Testing with Logical Operators
You can use `true` in conjunction with logical operators:
```bash
true && echo "This will always print."
```

## Tips
- Use `true` in scripts where you need a command that always succeeds, especially in loops or conditionals.
- It can be helpful in testing and debugging scripts where you want to temporarily disable certain commands without removing them.
- Remember that `true` does not produce any output, so if you need to see confirmation of execution, consider using `echo` alongside it.