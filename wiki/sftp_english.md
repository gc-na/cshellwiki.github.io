# [Linux] Bash sftp Uso: Securely transfer files over SSH

## Overview
The `sftp` (Secure File Transfer Protocol) command is a secure method for transferring files between computers over a network. It operates over SSH (Secure Shell), providing an encrypted connection to ensure the security of the data being transferred.

## Usage
The basic syntax of the `sftp` command is as follows:

```bash
sftp [options] [user@]host
```

## Common Options
- `-P port`: Specify the port to connect to on the remote host.
- `-o option`: Pass specific options to the SSH connection.
- `-r`: Recursively copy entire directories.
- `-v`: Enable verbose mode for debugging.

## Common Examples
Here are some practical examples of using the `sftp` command:

1. **Connect to a remote server:**
   ```bash
   sftp user@hostname
   ```

2. **Download a file from the remote server:**
   ```bash
   sftp user@hostname:/path/to/remote/file /path/to/local/destination
   ```

3. **Upload a file to the remote server:**
   ```bash
   sftp user@hostname
   put /path/to/local/file /path/to/remote/destination
   ```

4. **Download an entire directory:**
   ```bash
   sftp -r user@hostname:/path/to/remote/directory /path/to/local/destination
   ```

5. **List files in the remote directory:**
   ```bash
   sftp user@hostname
   ls /path/to/remote/directory
   ```

## Tips
- Always ensure that you are using the latest version of SSH and SFTP for improved security.
- Use the `-v` option to troubleshoot connection issues by providing detailed output.
- Consider using key-based authentication for a more secure and convenient login process.
- Regularly check permissions on your files and directories to maintain security during file transfers.