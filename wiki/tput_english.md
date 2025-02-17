# [Linux] Bash tput Uso: Control terminal display attributes

## Overview
The `tput` command is used in Bash to initialize or query the terminal capabilities. It allows users to control various aspects of terminal display, such as colors, cursor movement, and text formatting, making it a powerful tool for creating visually appealing command-line interfaces.

## Usage
The basic syntax of the `tput` command is as follows:

```bash
tput [options] [arguments]
```

## Common Options
- `setaf [n]`: Set the foreground color to the color number `n`.
- `setab [n]`: Set the background color to the color number `n`.
- `bold`: Enable bold text.
- `smso`: Start standout mode (usually bold or highlighted text).
- `rmso`: End standout mode.
- `cup [y] [x]`: Move the cursor to the specified position (y, x).
- `clear`: Clear the terminal screen.

## Common Examples
Here are some practical examples of using the `tput` command:

### Change Text Color
To change the text color to red:

```bash
tput setaf 1
echo "This text is red!"
tput sgr0  # Reset to default
```

### Change Background Color
To change the background color to blue:

```bash
tput setab 4
echo "This background is blue!"
tput sgr0  # Reset to default
```

### Bold Text
To print bold text:

```bash
tput bold
echo "This text is bold!"
tput sgr0  # Reset to default
```

### Move Cursor
To move the cursor to the 5th row and 10th column:

```bash
tput cup 5 10
echo "Cursor moved here!"
```

### Clear Screen
To clear the terminal screen:

```bash
tput clear
```

## Tips
- Always use `tput sgr0` after changing text attributes to reset them to default. This prevents subsequent text from inheriting the styles.
- You can combine multiple `tput` commands in a single script to create complex formatting.
- Use `tput -T <term>` to specify a terminal type if you're working in a non-standard environment.