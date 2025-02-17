# [Linux] Bash unalias uso: Remove command aliases

## Overview
The `unalias` command in Bash is used to remove existing aliases from the current shell session. Aliases are shortcuts for longer commands, and sometimes you may want to revert to the original command behavior by removing these shortcuts.

## Usage
The basic syntax of the `unalias` command is as follows:

```bash
unalias [options] [arguments]
```

## Common Options
- `-a`: Remove all aliases from the current session.
- `-m`: Remove aliases that match a specified pattern.

## Common Examples

1. **Remove a specific alias**:
   If you have an alias called `ll` that lists files in a detailed format, you can remove it with:
   ```bash
   unalias ll
   ```

2. **Remove multiple aliases**:
   To remove multiple aliases at once, you can specify them in the command:
   ```bash
   unalias ll gs
   ```

3. **Remove all aliases**:
   To clear all aliases from the current session, use the `-a` option:
   ```bash
   unalias -a
   ```

4. **Remove aliases matching a pattern**:
   If you want to remove aliases that start with `g`, you can use the `-m` option:
   ```bash
   unalias -m g*
   ```

## Tips
- Always check your current aliases with the `alias` command before removing them to avoid accidentally deleting important shortcuts.
- If you want to make sure an alias is removed permanently, consider removing it from your shell's configuration file (like `.bashrc` or `.bash_profile`).
- Use `unalias -a` with caution, as it will remove all aliases and may affect your workflow.