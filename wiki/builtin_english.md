# [Linux] Bash builtin `builtin`: Access shell builtins directly

## Overview
The `builtin` command in Bash allows users to execute shell built-in commands directly, bypassing any external commands that may have the same name. This is particularly useful when you want to ensure that you are using the shell's built-in version of a command rather than an external one.

## Usage
The basic syntax of the `builtin` command is as follows:

```bash
builtin [options] [command [arguments]]
```

## Common Options
- `-p`: This option allows you to use the `builtin` command to execute the specified command in a way that prevents any shell functions or aliases from being used.

## Common Examples

### Example 1: Using `builtin` with `echo`
To ensure you are using the built-in `echo` command, you can run:

```bash
builtin echo "This is a built-in echo command."
```

### Example 2: Using `builtin` with `type`
If you want to check the type of a command, you can use:

```bash
builtin type echo
```

This will show you whether `echo` is a built-in command or an external command.

### Example 3: Using `builtin` with `cd`
To change directories using the built-in `cd` command, you can execute:

```bash
builtin cd /path/to/directory
```

### Example 4: Using `builtin` with `exit`
To exit the shell using the built-in `exit` command, you can run:

```bash
builtin exit 0
```

## Tips
- Always use `builtin` when you want to avoid any potential conflicts with functions or aliases that may have the same name as the built-in command.
- Use the `-p` option if you want to ensure that the command executed is the built-in version, regardless of any user-defined functions or aliases.
- Familiarize yourself with the built-in commands available in your shell to make the most of the `builtin` command.