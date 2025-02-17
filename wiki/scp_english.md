# [Linux] Bash scp Uso: Securely copy files between hosts

## Overview
The `scp` (Secure Copy Protocol) command is used to securely transfer files and directories between two hosts over a network. It leverages SSH (Secure Shell) for data transfer, ensuring that the files are encrypted during the transfer process.

## Usage
The basic syntax of the `scp` command is as follows:

```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: Recursively copy entire directories.
- `-P port`: Specify the port to connect to on the remote host (note the uppercase 'P').
- `-i identity_file`: Select the file from which the identity (private key) for public key authentication is read.
- `-v`: Enable verbose mode, which provides detailed information about the connection process.
- `-q`: Quiet mode, which suppresses the progress meter and non-error messages.

## Common Examples
1. **Copy a file from local to remote:**
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. **Copy a file from remote to local:**
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. **Copy an entire directory from local to remote:**
   ```bash
   scp -r /path/to/local/directory user@remote_host:/path/to/remote/
   ```

4. **Copy a file using a specific port:**
   ```bash
   scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/
   ```

5. **Copy a file using a specific identity file:**
   ```bash
   scp -i /path/to/private_key user@remote_host:/path/to/remote/file.txt /path/to/local/
   ```

## Tips
- Always ensure that you have the correct permissions to access the files and directories you are transferring.
- Use the `-v` option for troubleshooting connection issues; it can provide helpful insights.
- When transferring large files, consider using the `-C` option to enable compression, which can speed up the transfer.
- Be cautious with the `-r` option to avoid unintentionally copying large directories.