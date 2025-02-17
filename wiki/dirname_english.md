# [Linux] Bash dirname Usage: Extract directory path from a file path

## Overview
The `dirname` command in Bash is used to extract the directory path from a given file path. It removes the last component of the path, returning only the directory portion. This is particularly useful for scripting and file manipulation tasks where you need to work with directory paths.

## Usage
The basic syntax of the `dirname` command is as follows:

```bash
dirname [options] [arguments]
```

## Common Options
- `-z`, `--zero`: This option allows the command to handle input paths that are separated by a null character instead of a newline.
- `--help`: Displays help information about the command and its options.
- `--version`: Shows the version of the `dirname` command.

## Common Examples

1. **Basic Usage**
   Extract the directory from a file path:
   ```bash
   dirname /home/user/documents/file.txt
   ```
   Output:
   ```
   /home/user/documents
   ```

2. **Using with a Relative Path**
   Extract the directory from a relative file path:
   ```bash
   dirname ./projects/code/script.sh
   ```
   Output:
   ```
   ./projects/code
   ```

3. **Handling Multiple Paths**
   You can provide multiple paths to `dirname`:
   ```bash
   dirname /var/log/syslog /etc/hosts
   ```
   Output:
   ```
   /var/log
   /etc
   ```

4. **Using with Variables**
   You can also use `dirname` with shell variables:
   ```bash
   FILE_PATH="/usr/local/bin/script.sh"
   echo $(dirname "$FILE_PATH")
   ```
   Output:
   ```
   /usr/local/bin
   ```

## Tips
- Always quote your file paths, especially if they contain spaces or special characters, to avoid unexpected behavior.
- Use `dirname` in scripts to dynamically build paths based on file locations, enhancing portability and flexibility.
- Combine `dirname` with other commands like `basename` to manipulate file paths effectively. For example:
  ```bash
  DIR=$(dirname "$FILE_PATH")
  BASENAME=$(basename "$FILE_PATH")
  echo "Directory: $DIR, File: $BASENAME"
  ```