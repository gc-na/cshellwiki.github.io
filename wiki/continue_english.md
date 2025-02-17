# [Linux] Bash continue Usage: Control loop execution

## Overview
The `continue` command in Bash is used within loops to skip the current iteration and proceed to the next one. This allows you to bypass certain conditions or commands within the loop without terminating the entire loop.

## Usage
The basic syntax of the `continue` command is as follows:

```bash
continue [n]
```

Here, `n` is an optional argument that specifies how many levels of nested loops to skip. If not provided, it defaults to 1.

## Common Options
- `n`: Specifies the number of nested loops to skip. For example, `continue 2` will skip to the next iteration of the second outermost loop.

## Common Examples

### Example 1: Basic Usage
In this example, we use `continue` to skip even numbers in a loop.

```bash
for i in {1..10}; do
    if (( i % 2 == 0 )); then
        continue
    fi
    echo $i
done
```
*Output:*
```
1
3
5
7
9
```

### Example 2: Skipping Specific Conditions
Here, we skip processing when a variable equals a certain value.

```bash
for file in file1.txt file2.txt file3.txt; do
    if [[ $file == "file2.txt" ]]; then
        continue
    fi
    echo "Processing $file"
done
```
*Output:*
```
Processing file1.txt
Processing file3.txt
```

### Example 3: Nested Loops
In this example, we use `continue` to skip to the next iteration of the outer loop.

```bash
for i in {1..3}; do
    for j in {1..3}; do
        if (( j == 2 )); then
            continue 2
        fi
        echo "i: $i, j: $j"
    done
done
```
*Output:*
```
i: 1, j: 1
i: 1, j: 3
i: 2, j: 1
i: 2, j: 3
i: 3, j: 1
i: 3, j: 3
```

## Tips
- Use `continue` to enhance the readability of your loops by avoiding deeply nested conditional statements.
- Remember that `continue` only affects the loop it is called in; if you have nested loops, specify the level of the loop you want to continue.
- Combine `continue` with other control structures like `if` to create more complex loop behaviors.