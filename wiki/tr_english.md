# [Linux] Bash tr Usage: Translate or delete characters

## Overview
The `tr` command in Bash is a utility for translating or deleting characters from standard input. It reads input from a file or standard input, processes it according to specified rules, and outputs the modified text. This command is particularly useful for tasks such as character substitution, case conversion, and removing unwanted characters.

## Usage
The basic syntax of the `tr` command is as follows:

```bash
tr [options] [arguments]
```

## Common Options
- `-d`: Delete characters specified in the arguments.
- `-s`: Squeeze multiple adjacent occurrences of a character into a single occurrence.
- `-c`: Complement the set of characters specified in the arguments.
- `-t`: Translate characters, but only for the first occurrence.

## Common Examples

### 1. Translate lowercase to uppercase
To convert all lowercase letters in a text to uppercase:

```bash
echo "hello world" | tr 'a-z' 'A-Z'
```

### 2. Delete specific characters
To remove all vowels from a text:

```bash
echo "hello world" | tr -d 'aeiou'
```

### 3. Squeeze repeated characters
To replace multiple spaces with a single space:

```bash
echo "This    is    a    test." | tr -s ' '
```

### 4. Complement character set
To replace all characters except digits with a space:

```bash
echo "abc123def456" | tr -c '0-9' ' '
```

### 5. Translate characters
To replace specific characters, such as converting 'a' to '1' and 'b' to '2':

```bash
echo "abc" | tr 'ab' '12'
```

## Tips
- Always test your `tr` commands with sample input to ensure they behave as expected.
- Use `echo` or input redirection to provide data to `tr` for testing.
- Combine `tr` with other commands using pipes to create powerful command-line workflows.