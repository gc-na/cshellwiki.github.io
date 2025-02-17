# [Linux] Bash exit usage: Terminate a shell session

## Overview
The `exit` command in Bash is used to terminate a shell session. It allows users to exit from the current shell or script and can also return an exit status to the calling process. This is particularly useful in scripts to indicate success or failure.

## Usage
The basic syntax of the `exit` command is as follows:

```bash
exit [n]
```

Where `n` is an optional exit status code. If no status code is provided, the exit status of the last executed command is used.

## Common Options
- `n`: An optional numeric argument that specifies the exit status. By convention, a status of `0` indicates success, while any non-zero value indicates an error or abnormal termination.

## Common Examples

1. **Exiting a shell session:**
   To simply exit the current shell, you can use:
   ```bash
   exit
   ```

2. **Exiting with a specific status code:**
   To exit with a specific status code, for example, `1`, you can use:
   ```bash
   exit 1
   ```

3. **Using exit in a script:**
   In a Bash script, you might want to exit based on a condition:
   ```bash
   #!/bin/bash
   if [ ! -f "important_file.txt" ]; then
       echo "File not found!"
       exit 1
   fi
   echo "File found, continuing..."
   ```

4. **Exiting from a subshell:**
   If you are in a subshell and want to exit back to the parent shell:
   ```bash
   ( 
       echo "Inside subshell"
       exit 0
   )
   echo "Back in parent shell"
   ```

## Tips
- Always use meaningful exit status codes in scripts to help with debugging and error handling.
- Use `exit 0` to indicate successful completion of a script or command.
- Remember that exiting from a subshell will not affect the parent shell; it only terminates the subshell session.