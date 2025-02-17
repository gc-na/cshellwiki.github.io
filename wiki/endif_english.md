# [Linux] Bash endif equivalente: Conditional execution in scripts

## Overview
The `endif` command is used in Bash scripting to denote the end of a conditional block that was started with an `if` statement. It helps organize code by clearly marking the conclusion of a conditional structure, making scripts easier to read and maintain.

## Usage
The basic syntax of the `endif` command is as follows:

```bash
endif
```

Note that `endif` is not a standalone command in Bash; it is used to close an `if` block that was opened with `if` and optionally followed by `then`.

## Common Options
The `endif` command does not have options of its own, as it simply serves as a marker in the script. It is used in conjunction with the `if` command and its options.

## Common Examples

### Example 1: Basic if statement
```bash
if [ "$USER" = "admin" ]; then
    echo "Welcome, admin!"
endif
```

### Example 2: If-else statement
```bash
if [ "$AGE" -ge 18 ]; then
    echo "You are an adult."
else
    echo "You are a minor."
endif
```

### Example 3: Nested if statements
```bash
if [ "$STATUS" = "active" ]; then
    if [ "$ROLE" = "admin" ]; then
        echo "Admin access granted."
    endif
endif
```

## Tips
- Always ensure that every `if` statement has a corresponding `endif` to avoid syntax errors.
- Use indentation within your conditional blocks to improve readability.
- Remember that `endif` is not a command but a part of the structure; it should not be used outside of an `if` context.