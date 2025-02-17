# [Linux] Bash fc Usage: Edit and re-execute commands

## Overview
The `fc` command in Bash is used to list, edit, and re-execute commands from the shell's history. It allows users to quickly modify previous commands and run them again without retyping everything.

## Usage
The basic syntax of the `fc` command is as follows:

```bash
fc [options] [arguments]
```

## Common Options
- `-l`: List the commands from the history.
- `-r`: Reverses the order of the commands when listing.
- `-n`: Suppresses the command numbers when listing.
- `-s`: Re-execute the command without opening an editor.
- `-e`: Specify a different editor to use for editing the command.

## Common Examples

### List Recent Commands
To list the last 10 commands from your history, you can use:
```bash
fc -l -n -10
```

### Edit the Last Command
To edit the most recent command in your default text editor, simply run:
```bash
fc
```

### Re-execute a Specific Command
If you want to re-execute a specific command from your history, you can use:
```bash
fc -s 123
```
Replace `123` with the command number you want to re-execute.

### List Commands in Reverse Order
To list the last 5 commands in reverse order, use:
```bash
fc -l -r -5
```

### Use a Specific Editor
If you want to edit a command using a specific editor, such as `nano`, you can do:
```bash
fc -e nano
```

## Tips
- Use `fc -l` frequently to keep track of your command history and find commands you may want to reuse.
- If you often make the same changes to commands, consider using `fc -s` to quickly re-execute modified commands.
- Customize your default editor for `fc` by setting the `EDITOR` environment variable to your preferred text editor.