# [Linux] Bash test usage: Evaluate expressions and conditions

## Overview
The `test` command in Bash is used to evaluate expressions and conditions. It helps in making decisions in scripts by checking the status of files, comparing strings, and evaluating numerical expressions. Essentially, it returns a true (0) or false (1) exit status based on the evaluation.

## Usage
The basic syntax of the `test` command is as follows:

```bash
test [options] [arguments]
```

Alternatively, you can use the `[` command, which is a synonym for `test`:

```bash
[ expression ]
```

## Common Options
Here are some common options you can use with the `test` command:

- `-e FILE`: Returns true if the file exists.
- `-f FILE`: Returns true if the file exists and is a regular file.
- `-d DIRECTORY`: Returns true if the directory exists.
- `-r FILE`: Returns true if the file is readable.
- `-w FILE`: Returns true if the file is writable.
- `-x FILE`: Returns true if the file is executable.
- `STRING1 = STRING2`: Returns true if the two strings are equal.
- `STRING1 != STRING2`: Returns true if the two strings are not equal.
- `NUM1 -eq NUM2`: Returns true if the two numbers are equal.
- `NUM1 -ne NUM2`: Returns true if the two numbers are not equal.

## Common Examples

1. **Check if a file exists:**
   ```bash
   test -e myfile.txt && echo "File exists"
   ```

2. **Check if a directory exists:**
   ```bash
   test -d mydirectory && echo "Directory exists"
   ```

3. **Check if a file is readable:**
   ```bash
   test -r myfile.txt && echo "File is readable"
   ```

4. **Compare two strings:**
   ```bash
   test "hello" = "hello" && echo "Strings are equal"
   ```

5. **Check if a number is greater than another:**
   ```bash
   test 5 -gt 3 && echo "5 is greater than 3"
   ```

6. **Using the `[` synonym:**
   ```bash
   [ -f myfile.txt ] && echo "It's a regular file"
   ```

## Tips
- Use `&&` and `||` to combine multiple test commands for more complex conditions.
- Remember that `test` returns an exit status, which can be useful in conditional statements like `if`.
- Use quotes around strings to avoid issues with spaces or special characters.
- For readability, consider using the `[` syntax, as it can make your scripts easier to understand.