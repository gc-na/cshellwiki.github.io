# [Linux] Bash expr Usage Equivalent: Evaluate expressions and perform calculations

## Overview
The `expr` command in Bash is used for evaluating expressions and performing calculations. It can handle arithmetic operations, string manipulations, and logical comparisons, making it a versatile tool for scripting and command-line tasks.

## Usage
The basic syntax of the `expr` command is as follows:

```bash
expr [options] [arguments]
```

## Common Options
- `+` : Addition
- `-` : Subtraction
- `*` : Multiplication (must be escaped as `\*` or quoted)
- `/` : Division
- `%` : Modulus
- `=` : String comparison for equality
- `!=` : String comparison for inequality
- `>` : Greater than comparison
- `<` : Less than comparison
- `length` : Returns the length of a string

## Common Examples
Here are some practical examples of using the `expr` command:

### Arithmetic Operations
1. **Addition**
   ```bash
   expr 5 + 3
   ```
   Output: `8`

2. **Subtraction**
   ```bash
   expr 10 - 4
   ```
   Output: `6`

3. **Multiplication**
   ```bash
   expr 7 \* 6
   ```
   Output: `42`

4. **Division**
   ```bash
   expr 20 / 4
   ```
   Output: `5`

5. **Modulus**
   ```bash
   expr 10 % 3
   ```
   Output: `1`

### String Operations
1. **String Length**
   ```bash
   expr length "Hello World"
   ```
   Output: `11`

2. **String Comparison**
   ```bash
   expr "apple" = "apple"
   ```
   Output: `1` (true)

3. **Inequality Comparison**
   ```bash
   expr "banana" != "apple"
   ```
   Output: `1` (true)

### Logical Comparisons
1. **Greater Than**
   ```bash
   expr 5 \> 3
   ```
   Output: `1` (true)

2. **Less Than**
   ```bash
   expr 2 \< 4
   ```
   Output: `1` (true)

## Tips
- Always remember to escape the asterisk `*` when performing multiplication to avoid shell interpretation.
- Use parentheses to group expressions for clarity, especially in complex calculations.
- `expr` returns `0` for false and `1` for true in logical comparisons, which can be useful in conditional statements.
- Consider using `$(())` for arithmetic operations in Bash as it is often more straightforward and easier to read.