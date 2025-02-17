# [Linux] Bash head usage: Display the beginning of files

## Overview
The `head` command in Bash is used to display the first few lines of a file or standard input. By default, it shows the first 10 lines, making it a useful tool for quickly previewing the contents of a file without opening it entirely.

## Usage
The basic syntax of the `head` command is as follows:

```bash
head [options] [arguments]
```

## Common Options
- `-n NUM`: Display the first NUM lines of each file. For example, `-n 5` shows the first 5 lines.
- `-c NUM`: Display the first NUM bytes of each file instead of lines.
- `-q`: Suppress the output of file headers when multiple files are being processed.
- `-v`: Always output headers giving file names, even if there is only one file.

## Common Examples
Here are some practical examples of using the `head` command:

1. Display the first 10 lines of a file:
   ```bash
   head filename.txt
   ```

2. Display the first 5 lines of a file:
   ```bash
   head -n 5 filename.txt
   ```

3. Display the first 20 bytes of a file:
   ```bash
   head -c 20 filename.txt
   ```

4. Display the first 10 lines of multiple files:
   ```bash
   head file1.txt file2.txt
   ```

5. Display the first 10 lines of a file and include the file name:
   ```bash
   head -v filename.txt
   ```

## Tips
- Use `head` in combination with other commands, like `grep`, to quickly find the beginning of matching lines.
- If you want to preview a large file, consider using `head` to limit the output and avoid overwhelming your terminal.
- Remember that `head` can read from standard input, so you can pipe output from other commands into it for quick previews. For example:
  ```bash
  ls -l | head
  ```