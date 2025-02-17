# [Linux] Bash mkfifo Uso: Create named pipes for inter-process communication

## Overview
The `mkfifo` command in Bash is used to create named pipes, which are special types of files that allow for inter-process communication. Named pipes enable processes to communicate with each other by reading from and writing to the same file, facilitating data transfer.

## Usage
The basic syntax of the `mkfifo` command is as follows:

```bash
mkfifo [options] [arguments]
```

## Common Options
- `-m, --mode=MODE`: Set the file mode (permissions) for the created FIFO. This option allows you to specify who can read from or write to the pipe.
- `--help`: Display help information about the command and its options.
- `--version`: Show the version information of the `mkfifo` command.

## Common Examples

1. **Create a simple named pipe:**
   ```bash
   mkfifo mypipe
   ```

2. **Create a named pipe with specific permissions:**
   ```bash
   mkfifo -m 600 mypipe
   ```
   This command creates a named pipe called `mypipe` with read and write permissions for the owner only.

3. **Using a named pipe in a command:**
   ```bash
   cat mypipe &
   echo "Hello, World!" > mypipe
   ```
   In this example, `cat` reads from `mypipe` in the background, while `echo` writes "Hello, World!" to the pipe.

4. **Creating multiple named pipes at once:**
   ```bash
   mkfifo pipe1 pipe2
   ```
   This command creates two named pipes, `pipe1` and `pipe2`, in a single command.

## Tips
- Always ensure that the named pipe is created before attempting to read from or write to it.
- Use appropriate permissions to control access to the named pipe, especially in multi-user environments.
- Remember that reading from a named pipe will block until there is data to read, and writing will block until there is a reader. This can be useful for synchronizing processes.