# [Linux] Bash uniq Usage: Remove duplicate lines from sorted files

## Overview
The `uniq` command in Bash is used to filter out or report repeated lines in a sorted file. It is particularly useful for processing text files where you want to eliminate duplicate entries or count occurrences of unique lines.

## Usage
The basic syntax of the `uniq` command is as follows:

```bash
uniq [options] [input_file] [output_file]
```

If no input file is specified, `uniq` reads from standard input.

## Common Options
- `-c`: Prefix each line with the number of occurrences.
- `-d`: Only print duplicate lines.
- `-u`: Only print unique lines (lines that are not repeated).
- `-i`: Ignore case differences when comparing lines.
- `-w N`: Compare only the first N characters of each line.

## Common Examples

1. **Remove duplicates from a sorted file:**
   ```bash
   uniq sorted_file.txt
   ```

2. **Count occurrences of each line:**
   ```bash
   uniq -c sorted_file.txt
   ```

3. **Display only duplicate lines:**
   ```bash
   uniq -d sorted_file.txt
   ```

4. **Display only unique lines:**
   ```bash
   uniq -u sorted_file.txt
   ```

5. **Ignore case when filtering duplicates:**
   ```bash
   uniq -i sorted_file.txt
   ```

6. **Compare only the first 5 characters of each line:**
   ```bash
   uniq -w 5 sorted_file.txt
   ```

## Tips
- Always sort your file before using `uniq`, as it only removes consecutive duplicate lines.
- Use `sort -u` as a combination to sort and remove duplicates in one step.
- Pipe output from other commands into `uniq` for streamlined processing, like so:
  ```bash
  cat file.txt | sort | uniq
  ```
- Remember that `uniq` does not modify the original file; it outputs the results to standard output or a specified output file.