# [Linux] Bash uname Usage Equivalent: Display system information

## Overview
The `uname` command in Bash is used to display system information. It provides details about the operating system and the hardware on which it is running, making it a useful tool for system administrators and users who need to gather information about their environment.

## Usage
The basic syntax of the `uname` command is as follows:

```
uname [options] [arguments]
```

## Common Options
Here are some common options you can use with the `uname` command:

- `-a`: Displays all available system information.
- `-s`: Shows the kernel name.
- `-n`: Displays the network node hostname.
- `-r`: Shows the kernel release.
- `-v`: Displays the kernel version.
- `-m`: Shows the machine hardware name.
- `-p`: Displays the processor type (if available).
- `-i`: Shows the hardware platform (if available).
- `-o`: Displays the operating system.

## Common Examples

1. **Display all system information:**
   ```bash
   uname -a
   ```

2. **Show the kernel name:**
   ```bash
   uname -s
   ```

3. **Display the kernel release:**
   ```bash
   uname -r
   ```

4. **Show the machine hardware name:**
   ```bash
   uname -m
   ```

5. **Display the operating system:**
   ```bash
   uname -o
   ```

## Tips
- Use `uname -a` for a comprehensive overview of your system in one command.
- Combine `uname` with other commands in scripts to automate system checks.
- Remember that some options may not return information on all systems, depending on the configuration and available data.