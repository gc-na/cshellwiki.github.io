# [Linux] Bash cal Usage: Display a calendar

## Overview
The `cal` command in Bash is used to display a calendar in the terminal. It can show the current month, a specific month, or an entire year, making it a handy tool for quick date references.

## Usage
The basic syntax of the `cal` command is as follows:

```bash
cal [options] [arguments]
```

## Common Options
- `-m`: Display the calendar in a more compact format.
- `-y`: Show the calendar for the entire current year.
- `-3`: Display the previous, current, and next month.
- `-j`: Show the Julian calendar.
- `-A <num>`: Show <num> months after the specified month.
- `-B <num>`: Show <num> months before the specified month.

## Common Examples
Here are some practical examples of how to use the `cal` command:

1. **Display the current month:**
   ```bash
   cal
   ```

2. **Display a specific month and year (e.g., March 2023):**
   ```bash
   cal 03 2023
   ```

3. **Display the entire current year:**
   ```bash
   cal -y
   ```

4. **Display the previous, current, and next month:**
   ```bash
   cal -3
   ```

5. **Display the calendar with Julian dates:**
   ```bash
   cal -j
   ```

6. **Display the calendar for the next 2 months after January 2023:**
   ```bash
   cal -A 2 01 2023
   ```

## Tips
- Use `cal -m` for a more compact view if you're short on terminal space.
- Combine options for more customized views, such as `cal -3 -B 1` to see the previous month and the next two months.
- Remember that the months are specified numerically (01 for January, 02 for February, etc.), which can help avoid confusion when entering dates.