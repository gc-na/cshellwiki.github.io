# [Linux] Bash export uso equivalente: Set environment variables

## Overview
The `export` command in Bash is used to set environment variables that can be accessed by child processes. When a variable is exported, it becomes part of the environment for any subsequent commands or scripts executed in the current shell session.

## Usage
The basic syntax of the `export` command is as follows:

```bash
export [options] [arguments]
```

## Common Options
- `-p`: Displays all exported variables in the current shell session.
- `-n`: Unsets the export attribute for the specified variable, making it local to the current shell.
- `-f`: Exports functions defined in the current shell.

## Common Examples

### Example 1: Exporting a simple variable
To export a variable named `MY_VAR` with the value `Hello World`, you can use:

```bash
MY_VAR="Hello World"
export MY_VAR
```

### Example 2: Exporting and using a variable in a child process
After exporting a variable, you can access it in a child process, such as a subshell:

```bash
export MY_VAR="Hello World"
bash -c 'echo $MY_VAR'
```

### Example 3: Listing all exported variables
To see all currently exported variables, use the `-p` option:

```bash
export -p
```

### Example 4: Unsetting an exported variable
If you want to remove the export attribute from a variable, you can use the `-n` option:

```bash
export MY_VAR="Hello World"
export -n MY_VAR
```

### Example 5: Exporting a function
You can also export functions to make them available in child processes:

```bash
my_function() {
    echo "This is a function"
}
export -f my_function
bash -c 'my_function'
```

## Tips
- Always remember to export variables if you need them in child processes.
- Use `export -p` to check which variables are currently exported.
- Be cautious when unsetting variables, as it may affect scripts or commands that rely on them.