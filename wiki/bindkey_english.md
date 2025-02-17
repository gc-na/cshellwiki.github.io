# [Linux] Bash bindkey用法: 绑定键盘快捷键

## Overview
The `bindkey` command is used in the Zsh shell to set or display key bindings. It allows users to customize keyboard shortcuts for various commands and functions, enhancing the efficiency of command-line interactions.

## Usage
The basic syntax of the `bindkey` command is as follows:

```bash
bindkey [options] [arguments]
```

## Common Options
- `-L`: List all current key bindings.
- `-s`: Specify a string to be sent when a key sequence is pressed.
- `-e`: Use Emacs-style key bindings.
- `-v`: Use Vi-style key bindings.

## Common Examples
1. **List Current Key Bindings**
   ```bash
   bindkey -L
   ```

2. **Set a Key Binding for a Command**
   ```bash
   bindkey '^x' 'exit'
   ```
   This binds `Ctrl+x` to the `exit` command.

3. **Set a Key Binding for a Custom Function**
   ```bash
   bindkey '^g' 'git status'
   ```
   This binds `Ctrl+g` to run `git status`.

4. **Use Vi Mode Key Bindings**
   ```bash
   bindkey -v
   ```
   This switches the key bindings to Vi mode.

5. **Bind a Key Sequence to Insert Text**
   ```bash
   bindkey '^[o' 'echo "Hello, World!"'
   ```
   This binds the `Esc` followed by `o` to insert the text "Hello, World!".

## Tips
- Always check your current key bindings using `bindkey -L` before making changes to avoid conflicts.
- Use descriptive names for your custom key bindings to remember their functions easily.
- Experiment with different modes (Emacs and Vi) to find which one suits your workflow best.