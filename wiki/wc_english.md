# [Linux] Bash wc Usage: Count lines, words, and characters in files

## Overview
The `wc` command, short for "word count," is a utility in Unix-like operating systems that counts the number of lines, words, and characters in a text file. It can be used to quickly gather statistics about the content of files or standard input.

## Usage
The basic syntax of the `wc` command is as follows:

```bash
wc [options] [arguments]
```

## Common Options
- `-l`: Count the number of lines.
- `-w`: Count the number of words.
- `-c`: Count the number of bytes (characters).
- `-m`: Count the number of characters (useful for multibyte characters).
- `-L`: Print the length of the longest line.

## Common Examples
Here are some practical examples of using the `wc` command:

1. **Count lines in a file:**
   ```bash
   wc -l filename.txt
   ```

2. **Count words in a file:**
   ```bash
   wc -w filename.txt
   ```

3. **Count characters in a file:**
   ```bash
   wc -c filename.txt
   ```

4. **Count lines, words, and characters in a file:**
   ```bash
   wc filename.txt
   ```

5. **Count lines in multiple files:**
   ```bash
   wc -l file1.txt file2.txt
   ```

6. **Count the longest line in a file:**
   ```bash
   wc -L filename.txt
   ```

## Tips
- Combine options to get multiple counts at once, for example, `wc -l -w filename.txt`.
- Use `wc` with pipes to count output from other commands, like `echo "Hello World" | wc -w` to count words in the output.
- When working with large files, consider using `head` or `tail` in combination with `wc` to focus on specific sections of the file.