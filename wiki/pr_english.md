# [Linux] Bash pr: Format text for printing

## Overview
The `pr` command in Bash is used to format text files for printing. It arranges the content into pages, adds headers, and can even manage multiple columns, making it easier to read and print documents.

## Usage
The basic syntax of the `pr` command is as follows:

```bash
pr [options] [arguments]
```

## Common Options
- `-h, --header=STRING`: Specify a custom header for each page.
- `-l, --length=NUMBER`: Set the number of lines per page.
- `-n, --number`: Number the output lines.
- `-t, --omit-header`: Omit the header and footer from the output.
- `-s, --separator=STRING`: Specify a string to use as a column separator.

## Common Examples
Here are some practical examples of using the `pr` command:

1. **Basic Formatting**:
   Format a text file for printing with default settings.
   ```bash
   pr myfile.txt
   ```

2. **Custom Header**:
   Add a custom header to the output.
   ```bash
   pr -h "My Custom Header" myfile.txt
   ```

3. **Set Page Length**:
   Change the number of lines per page to 50.
   ```bash
   pr -l 50 myfile.txt
   ```

4. **Numbering Lines**:
   Number the lines in the output.
   ```bash
   pr -n myfile.txt
   ```

5. **Multiple Columns**:
   Format the output in two columns.
   ```bash
   pr -2 myfile.txt
   ```

## Tips
- Use `pr` in combination with other commands like `less` or `more` to view the formatted output without printing.
- Experiment with different column settings to find the layout that works best for your document.
- Remember to check the output before printing to ensure it meets your formatting needs.