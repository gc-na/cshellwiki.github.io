# [Linux] Bash hexdump Usage: Display file contents in hexadecimal format

## Overview
The `hexdump` command is a utility that allows users to view the binary data of files in a human-readable hexadecimal format. It can be particularly useful for debugging, analyzing binary files, or inspecting the raw data of files.

## Usage
The basic syntax of the `hexdump` command is as follows:

```bash
hexdump [options] [arguments]
```

## Common Options
- `-C`: Canonical hex+ASCII display. This option shows both the hexadecimal representation and the ASCII equivalent side by side.
- `-n <number>`: Limits the output to the first `<number>` bytes of the file.
- `-v`: Displays all data, including repeated lines. By default, `hexdump` may condense repeated lines.
- `-e <format>`: Allows custom formatting of the output. You can specify how to display the data.

## Common Examples

### Example 1: Basic Hexdump
To display the hexadecimal representation of a file named `example.bin`:

```bash
hexdump example.bin
```

### Example 2: Canonical Hex+ASCII Display
To view the file `example.bin` in canonical format:

```bash
hexdump -C example.bin
```

### Example 3: Limit Output to First 16 Bytes
To limit the output to the first 16 bytes of `example.bin`:

```bash
hexdump -n 16 example.bin
```

### Example 4: Display All Data
To ensure all data is displayed, including repeated lines:

```bash
hexdump -v example.bin
```

### Example 5: Custom Formatting
To display the data in a custom format, for example, as 4-byte integers:

```bash
hexdump -e '4/4 "%08x " "\n"' example.bin
```

## Tips
- Use the `-C` option for a clearer understanding of the binary data, as it provides both hex and ASCII views.
- When working with large files, consider using the `-n` option to limit the output, making it easier to analyze specific sections.
- Experiment with the `-e` option to tailor the output format to your needs, especially when dealing with structured binary data.