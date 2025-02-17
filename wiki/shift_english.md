# [Linux] Bash shift用法: Shift positional parameters

## Overview
The `shift` command in Bash is used to manipulate positional parameters. It shifts the values of the positional parameters to the left, effectively discarding the first parameter and moving all others one position down. This is particularly useful in scripts where you need to process command-line arguments sequentially.

## Usage
The basic syntax of the `shift` command is as follows:

```bash
shift [n]
```

Where `n` is an optional argument that specifies how many positions to shift. If `n` is not provided, it defaults to 1.

## Common Options
- `n`: An optional numeric argument that indicates how many positions to shift the positional parameters. If omitted, it shifts by one.

## Common Examples

### Example 1: Basic Shift
This example demonstrates a simple shift of positional parameters.

```bash
#!/bin/bash
set -- one two three four
echo "Before shift: $1 $2 $3 $4"
shift
echo "After shift: $1 $2 $3 $4"
```

**Output:**
```
Before shift: one two three four
After shift: two three four
```

### Example 2: Shifting Multiple Positions
You can specify how many positions to shift.

```bash
#!/bin/bash
set -- apple banana cherry date
echo "Before shift: $1 $2 $3 $4"
shift 2
echo "After shift: $1 $2 $3 $4"
```

**Output:**
```
Before shift: apple banana cherry date
After shift: cherry date
```

### Example 3: Looping Through Arguments
Using `shift` in a loop to process all command-line arguments.

```bash
#!/bin/bash
echo "Processing arguments:"
while [ "$#" -gt 0 ]; do
    echo "Argument: $1"
    shift
done
```

**Usage:**
```bash
./script.sh arg1 arg2 arg3
```

**Output:**
```
Processing arguments:
Argument: arg1
Argument: arg2
Argument: arg3
```

## Tips
- Use `shift` when you need to process command-line arguments one at a time in a loop.
- Always check the number of positional parameters (`$#`) before shifting to avoid errors.
- Combine `shift` with other commands like `case` or `if` to create more complex argument processing logic.