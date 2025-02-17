# [Linux] Bash hash uso: Manage command hash table

## Overview
The `hash` command in Bash is used to manage the hash table of commands. When you execute a command, Bash remembers its location in the filesystem, which can speed up future executions of the same command. The `hash` command allows you to view, add, or remove entries from this hash table.

## Usage
The basic syntax of the `hash` command is as follows:

```bash
hash [options] [arguments]
```

## Common Options
- `-r`: Clears the hash table, removing all entries.
- `-p`: Specifies a path for the command to hash.
- `-l`: Lists the current contents of the hash table.

## Common Examples

### Listing Current Hash Table
To view the current entries in the hash table, simply run:

```bash
hash
```

### Clearing the Hash Table
To remove all entries from the hash table, use the `-r` option:

```bash
hash -r
```

### Adding a Command to the Hash Table
You can add a specific command to the hash table with the `-p` option:

```bash
hash -p /usr/local/bin/mycommand mycommand
```

### Listing Hash Table with Full Paths
To see the commands along with their full paths, use the `-l` option:

```bash
hash -l
```

## Tips
- Use `hash` after changing your PATH or installing new software to ensure Bash recognizes the new command locations.
- Regularly clear the hash table if you frequently change command locations to avoid potential conflicts.
- Use `hash` to quickly check if a command is already cached, which can save time when executing frequently used commands.