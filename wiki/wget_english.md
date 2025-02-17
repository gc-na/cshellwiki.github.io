# [Linux] Bash wget Uso: Download files from the web

## Overview
The `wget` command is a powerful utility for downloading files from the web. It supports HTTP, HTTPS, and FTP protocols, making it versatile for retrieving content from various sources. `wget` is non-interactive, meaning it can work in the background without requiring user input, which is particularly useful for automated scripts.

## Usage
The basic syntax of the `wget` command is as follows:

```bash
wget [options] [arguments]
```

## Common Options
Here are some commonly used options with `wget`:

- `-O [filename]`: Save the downloaded file with a specified name.
- `-q`: Run in quiet mode, suppressing output.
- `-c`: Continue an incomplete download.
- `-r`: Enable recursive downloading, useful for downloading entire websites.
- `--limit-rate=[amount]`: Limit the download speed to a specified rate.
- `-P [directory]`: Specify a directory to save the downloaded files.

## Common Examples

1. **Download a single file:**
   ```bash
   wget https://example.com/file.zip
   ```

2. **Download a file and save it with a specific name:**
   ```bash
   wget -O myfile.zip https://example.com/file.zip
   ```

3. **Continue an interrupted download:**
   ```bash
   wget -c https://example.com/largefile.zip
   ```

4. **Download an entire website recursively:**
   ```bash
   wget -r https://example.com
   ```

5. **Limit the download speed:**
   ```bash
   wget --limit-rate=200k https://example.com/largefile.zip
   ```

6. **Download files to a specific directory:**
   ```bash
   wget -P /path/to/directory https://example.com/file.zip
   ```

## Tips
- Use the `-q` option for scripts to reduce output clutter.
- Combine `-c` with `-P` to manage downloads in specific directories without losing progress.
- When downloading large files, consider using `--limit-rate` to avoid saturating your internet connection.
- For recursive downloads, be cautious with the depth of recursion to avoid downloading unnecessary files. Use `--level=[number]` to control this.