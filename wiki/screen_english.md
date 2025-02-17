# [Linux] Bash screen usage: Manage multiple terminal sessions

## Overview
The `screen` command is a terminal multiplexer that allows users to manage multiple terminal sessions from a single window. It enables you to run processes in the background, detach from sessions, and later reattach to them, making it particularly useful for long-running tasks or remote server management.

## Usage
The basic syntax of the `screen` command is as follows:

```bash
screen [options] [arguments]
```

## Common Options
- `-S <session_name>`: Start a new session with a specified name.
- `-d -r <session_name>`: Detach and reattach to a session by name.
- `-list`: List all active screen sessions.
- `-X <command>`: Send a command to a specific screen session.
- `-h <lines>`: Set the scrollback buffer to a specified number of lines.

## Common Examples

### Start a New Screen Session
To start a new screen session, simply run:

```bash
screen
```

### Start a Named Session
To create a session with a specific name:

```bash
screen -S mysession
```

### Detach from a Session
To detach from the current session and leave it running in the background, press:

```
Ctrl + A, then D
```

### Reattach to a Session
To reattach to a previously detached session:

```bash
screen -r mysession
```

### List Active Sessions
To see all active screen sessions:

```bash
screen -list
```

### Send a Command to a Session
To send a command to a specific session:

```bash
screen -S mysession -X stuff "echo Hello World\n"
```

## Tips
- Use named sessions to easily identify and manage multiple screen sessions.
- Detach sessions before logging out of a remote server to keep processes running.
- Familiarize yourself with keyboard shortcuts for efficient navigation within screen.
- Consider using the `-h` option to increase the scrollback buffer for better access to previous output.