# [Linux] Bash readonly用法: Prevent variable modification

## Overview
The `readonly` command in Bash is used to mark variables or functions as unchangeable. Once a variable is declared as readonly, its value cannot be modified or unset during the session, which helps in maintaining the integrity of important data.

## Usage
The basic syntax of the `readonly` command is as follows:

```bash
readonly [options] [arguments]
```

## Common Options
- `-p`: Display a list of all readonly variables and functions in the current shell session.

## Common Examples

### Example 1: Declaring a readonly variable
To declare a variable as readonly, you can use the following command:

```bash
readonly MY_VAR="Hello World"
```

After executing this command, trying to modify `MY_VAR` will result in an error:

```bash
MY_VAR="New Value"  # This will produce an error
```

### Example 2: Listing readonly variables
To see all the readonly variables in your current shell session, use the `-p` option:

```bash
readonly -p
```

This will output a list of all readonly variables and their values.

### Example 3: Declaring a readonly function
You can also declare a function as readonly, preventing it from being redefined:

```bash
readonly my_function() {
    echo "This is a readonly function."
}
```

Attempting to redefine `my_function` will result in an error:

```bash
my_function() {
    echo "Trying to redefine."  # This will produce an error
}
```

## Tips
- Use `readonly` for critical variables that should not change throughout your script to avoid accidental modifications.
- Remember that `readonly` applies only to the current shell session; if you start a new session, the variables will not retain their readonly status unless explicitly set again.
- You can unset a readonly variable or function only by using the `unset` command in a subshell or by exiting the current session.