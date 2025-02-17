# [Linux] Bash pushd Usage: Navigate directories easily

## Overview
The `pushd` command in Bash is used to change the current directory while simultaneously saving the previous directory on a stack. This allows users to easily switch back to the original directory using the `popd` command.

## Usage
The basic syntax of the `pushd` command is as follows:

```bash
pushd [options] [arguments]
```

## Common Options
- `+n`: Rotate the directory stack to the right, where `n` is the index of the directory you want to switch to.
- `-n`: Rotate the directory stack to the left, where `n` is the index of the directory you want to switch to.
- `-q`: Suppress the output of the directory stack after the operation.

## Common Examples

1. **Change to a directory and save the current one:**
   ```bash
   pushd /path/to/directory
   ```

2. **Switch to a specific directory in the stack:**
   ```bash
   pushd +1
   ```

3. **Return to the previous directory using popd:**
   ```bash
   popd
   ```

4. **Suppress output while changing directories:**
   ```bash
   pushd -q /another/path
   ```

5. **View the current directory stack:**
   ```bash
   dirs
   ```

## Tips
- Use `dirs` to view the current directory stack and understand your navigation history.
- Combine `pushd` with `popd` for efficient directory navigation without losing your place.
- Remember that you can use `pushd` with relative paths, making it flexible for quick navigation.