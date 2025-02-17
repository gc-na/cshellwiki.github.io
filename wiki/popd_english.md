# [Linux] Bash popd Usage: Manage directory stack

## Overview
The `popd` command in Bash is used to remove the top directory from the directory stack, effectively changing the current working directory to the new top directory. This command is particularly useful for navigating between multiple directories without needing to type out full paths.

## Usage
The basic syntax of the `popd` command is as follows:

```bash
popd [options]
```

## Common Options
- `-n`: This option prevents the directory stack from being changed, allowing you to view the current stack without affecting it.
- `+n`: This option allows you to specify a directory to pop from the stack based on its position. For example, `+1` would pop the second directory in the stack.

## Common Examples

1. **Basic Usage**: Pop the top directory from the stack and change to it.
   ```bash
   popd
   ```

2. **Using with Directory Stack**: Push a directory onto the stack and then pop it.
   ```bash
   pushd /path/to/directory
   popd
   ```

3. **Popping a Specific Directory**: Pop the second directory in the stack.
   ```bash
   popd +1
   ```

4. **Preventing Stack Change**: View the current stack without changing it.
   ```bash
   popd -n
   ```

## Tips
- Always use `pushd` before `popd` to ensure that the directory stack has entries to pop.
- You can view the current directory stack using the `dirs` command, which helps you keep track of your navigation.
- Combine `pushd` and `popd` for efficient directory navigation in scripts or during complex tasks.