# [Linux] Bash tmux uso: Terminal multiplexer for managing multiple sessions

## Overview
The `tmux` command is a terminal multiplexer that allows users to create, manage, and navigate between multiple terminal sessions from a single window. It is particularly useful for managing long-running processes, organizing workflows, and maintaining persistent sessions, even when disconnected.

## Usage
The basic syntax of the `tmux` command is as follows:

```bash
tmux [options] [arguments]
```

## Common Options
- `new`: Create a new session.
- `attach`: Attach to an existing session.
- `detach`: Detach from the current session.
- `list-sessions`: List all active tmux sessions.
- `kill-session`: Terminate a specified session.

## Common Examples
Here are some practical examples of using `tmux`:

1. **Create a new session:**
   ```bash
   tmux new -s mysession
   ```
   This command creates a new tmux session named "mysession".

2. **Attach to an existing session:**
   ```bash
   tmux attach -t mysession
   ```
   This command attaches to the session named "mysession".

3. **Detach from the current session:**
   Press `Ctrl + b`, then `d`. This will detach you from the current session while keeping it running in the background.

4. **List all active sessions:**
   ```bash
   tmux list-sessions
   ```
   This command displays all currently active tmux sessions.

5. **Kill a specific session:**
   ```bash
   tmux kill-session -t mysession
   ```
   This command terminates the session named "mysession".

## Tips
- Use `Ctrl + b` followed by `c` to create a new window within a session.
- Split windows vertically with `Ctrl + b` followed by `%` and horizontally with `Ctrl + b` followed by `"` to enhance multitasking.
- To navigate between panes, use `Ctrl + b` followed by the arrow keys.
- Customize your tmux configuration by editing the `~/.tmux.conf` file to set your preferred key bindings and options.