# [Linux] Bash sha256sum uso: Calculate SHA-256 checksums

## Overview
The `sha256sum` command is used to compute and verify SHA-256 checksums for files. This is particularly useful for ensuring data integrity by comparing the checksum of a file against a known value.

## Usage
The basic syntax of the `sha256sum` command is as follows:

```bash
sha256sum [options] [arguments]
```

## Common Options
- `-b`, `--binary`: Read the input data in binary mode.
- `-c`, `--check`: Read SHA-256 checksums from a file and verify them against the corresponding files.
- `-t`, `--text`: Read the input data in text mode (default).
- `--tag`: Create a BSD-style checksum output.

## Common Examples

### Calculate SHA-256 Checksum of a File
To compute the SHA-256 checksum of a file named `example.txt`, use:

```bash
sha256sum example.txt
```

### Verify a Checksum
If you have a file `checksums.txt` containing checksums, you can verify the files listed in it:

```bash
sha256sum -c checksums.txt
```

### Generate Checksum for Multiple Files
You can also generate checksums for multiple files at once:

```bash
sha256sum file1.txt file2.txt file3.txt
```

### Save Checksum to a File
To save the checksum output to a file, you can redirect the output:

```bash
sha256sum example.txt > example_checksum.txt
```

## Tips
- Always verify checksums after downloading files from the internet to ensure they haven't been tampered with.
- Use the `-c` option with a checksum file to automate the verification process for multiple files.
- For large files, consider using the `-b` option to ensure accurate checksum calculation in binary mode.