# [Linux] Bash dirs Uso equivalente: Manage directory stack

## Overview
The `dirs` command in Bash is used to display the list of currently stored directories in the directory stack. This stack allows users to navigate between directories more efficiently, especially when working with multiple directories in a session.

## Usage
The basic syntax of the `dirs` command is as follows:

```bash
dirs [options] [arguments]
```

## Common Options
- `-l`: Display the directory stack in a long format, showing the full path of each directory.
- `-p`: Print the directory stack without changing the current directory.
- `-c`: Clear the directory stack.

## Common Examples

1. **Display the current directory stack:**
   ```bash
   dirs
   ```

2. **Display the directory stack in long format:**
   ```bash
   dirs -l
   ```

3. **Clear the directory stack:**
   ```bash
   dirs -c
   ```

4. **Show the directory stack without changing the current directory:**
   ```bash
   dirs -p
   ```

5. **Push a new directory onto the stack and then display it:**
   ```bash
   cd /path/to/directory
   dirs
   ```

## Tips
- Use `pushd` and `popd` commands to manage your directory stack effectively. `pushd` adds a directory to the stack, while `popd` removes the top directory from the stack.
- Remember that the order of directories in the stack is important; the most recent directory is at the top.
- You can combine `dirs` with other commands to create shortcuts for navigating your file system.