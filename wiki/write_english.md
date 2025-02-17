# [Linux] Bash write uso: Send messages to users

## Overview
The `write` command in Bash allows you to send messages to other users who are logged into the same system. This is particularly useful for communication in multi-user environments, enabling quick exchanges of information without the need for email or other messaging services.

## Usage
The basic syntax of the `write` command is as follows:

```bash
write [username] [tty]
```

- `username`: The name of the user you want to send a message to.
- `tty`: (optional) The terminal device of the user. If not specified, it defaults to the user's current terminal.

To end your message, you can press `Ctrl+D`.

## Common Options
- `-n`: Suppresses the notification that the user is being written to.
- `-h`: Suppresses the message header.
- `-s`: Sends a message silently without displaying it on the sender's terminal.

## Common Examples

### Example 1: Sending a Message
To send a message to a user named `alice`, simply type:

```bash
write alice
```
After entering your message, press `Ctrl+D` to send it.

### Example 2: Specifying a Terminal
If you know that `bob` is logged in on terminal `pts/1`, you can send a message directly to that terminal:

```bash
write bob pts/1
```

### Example 3: Sending a Silent Message
To send a message without notifying the recipient, you can use the `-s` option:

```bash
write -s alice
```

### Example 4: Suppressing the Header
If you want to send a message without the header information, use the `-h` option:

```bash
write -h alice
```

## Tips
- Always check if the user is available before sending a message to avoid unnecessary interruptions.
- Use `who` or `w` command to see who is logged in and their terminal information.
- Remember that messages sent via `write` can be seen by anyone who has access to the terminal, so avoid sending sensitive information.