# [English] Bash ftp Usage: Transfer files over a network

## Overview
The `ftp` command is a standard network protocol used to transfer files between a client and a server over the Internet or an intranet. It allows users to upload and download files, manage directories, and perform various file operations on remote systems.

## Usage
The basic syntax of the `ftp` command is as follows:

```bash
ftp [options] [arguments]
```

## Common Options
- `-i`: Turns off interactive prompting during multiple file transfers.
- `-n`: Restricts automatic login upon initial connection.
- `-v`: Enables verbose mode, providing detailed information about the transfer process.
- `-p`: Enables passive mode, which is useful for navigating firewalls.

## Common Examples

### Connecting to an FTP Server
To connect to an FTP server, use the following command:

```bash
ftp ftp.example.com
```

### Uploading a File
To upload a file from your local machine to the FTP server, use the `put` command after connecting:

```bash
put localfile.txt
```

### Downloading a File
To download a file from the FTP server to your local machine, use the `get` command:

```bash
get remotefile.txt
```

### Listing Files in a Directory
To list files in the current directory on the FTP server, use the `ls` command:

```bash
ls
```

### Changing Directories
To change the current directory on the FTP server, use the `cd` command:

```bash
cd /path/to/directory
```

## Tips
- Always use secure alternatives like `sftp` or `ftps` when transferring sensitive data to ensure encryption.
- Use the `-i` option for batch file transfers to avoid prompts for each file.
- Familiarize yourself with FTP commands such as `mget` and `mput` for transferring multiple files at once.