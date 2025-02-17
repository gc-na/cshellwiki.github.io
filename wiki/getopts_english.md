# [Linux] Bash getopts用法: 解析命令行选项

## Overview
The `getopts` command in Bash is used for parsing command-line options and arguments. It simplifies the process of handling user input in shell scripts, allowing you to define short options (like `-h`) and long options (like `--help`) easily.

## Usage
The basic syntax of the `getopts` command is as follows:

```bash
getopts optstring variable
```

- `optstring`: A string containing the valid options.
- `variable`: The name of the variable that will hold the option.

## Common Options
- `-a`: This option is used to specify an action.
- `-b`: This option can be used to set a boolean flag.
- `-c`: This option is often used to specify a count or a number.
- `-h`: Typically used to display help information.

## Common Examples

### Example 1: Basic Option Parsing
```bash
#!/bin/bash
while getopts "ab:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B selected with value: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```
In this example, the script handles options `-a` and `-b`, where `-b` requires an argument.

### Example 2: Using Multiple Options
```bash
#!/bin/bash
while getopts "abc" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B selected"
      ;;
    c)
      echo "Option C selected"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```
This script processes options `-a`, `-b`, and `-c`, allowing the user to select multiple options.

### Example 3: Help Option
```bash
#!/bin/bash
while getopts "h" opt; do
  case $opt in
    h)
      echo "Usage: script.sh [-a] [-b value] [-c]"
      exit 0
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```
Here, the `-h` option provides usage information for the script.

## Tips
- Always include a help option (`-h`) to guide users on how to use your script.
- Use `OPTARG` to access the argument provided with options that require one.
- Remember to handle invalid options gracefully to improve user experience.