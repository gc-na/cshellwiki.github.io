# [English] Bash 7z Usage: File compression and extraction tool

## Overview
The `7z` command is a powerful tool for compressing and extracting files. It is part of the 7-Zip software suite and supports a variety of archive formats, making it a versatile choice for managing file archives.

## Usage
The basic syntax of the `7z` command is as follows:

```
7z [options] [arguments]
```

## Common Options
- `a`: Add files to an archive.
- `x`: Extract files from an archive.
- `l`: List the contents of an archive.
- `d`: Delete files from an archive.
- `t`: Test the integrity of an archive.
- `u`: Update files in an archive.

## Common Examples
Here are some practical examples of using the `7z` command:

### Create a new archive
To create a new archive named `archive.7z` containing all files in the current directory:

```bash
7z a archive.7z *
```

### Extract an archive
To extract the contents of `archive.7z` into the current directory:

```bash
7z x archive.7z
```

### List contents of an archive
To list the files contained in `archive.7z`:

```bash
7z l archive.7z
```

### Delete a file from an archive
To delete `file.txt` from `archive.7z`:

```bash
7z d archive.7z file.txt
```

### Test an archive
To test the integrity of `archive.7z`:

```bash
7z t archive.7z
```

## Tips
- Always check the integrity of your archives after creating them using the `t` option.
- Use the `-p` option followed by a password to create encrypted archives, enhancing security.
- When compressing large directories, consider using the `-mx` option to set the compression level (e.g., `-mx=9` for maximum compression).
- Familiarize yourself with the various formats supported by `7z` to choose the best one for your needs.