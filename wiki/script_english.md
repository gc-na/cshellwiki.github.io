# [Linux] Bash script uso: Capture terminal sessions

## Overview
The `script` command in Bash is used to record a terminal session. It captures all the input and output of the terminal, allowing users to save their work or share their command-line activities with others. This can be particularly useful for creating tutorials, documenting processes, or debugging.

## Usage
The basic syntax of the `script` command is as follows:

```bash
script [options] [file]
```

Here, `[file]` is optional and specifies the name of the file where the session will be saved. If no file is provided, the output will be saved to a file named `typescript` by default.

## Common Options
- `-a`: Append the output to the file instead of overwriting it.
- `-c`: Run a command and save its output to the file.
- `-f`: Flush the output after each write, which can be useful for real-time monitoring.
- `-q`: Operate in quiet mode, suppressing the start and stop messages.

## Common Examples

### Basic Session Recording
To start recording a session and save it to a file named `session.log`:

```bash
script session.log
```

### Appending to an Existing File
To append the output of a new session to an existing file:

```bash
script -a session.log
```

### Recording a Specific Command
To record the output of a specific command, such as `ls`, and save it to a file:

```bash
script -c "ls -l" command_output.log
```

### Real-time Monitoring
To record a session while ensuring that the output is flushed in real-time:

```bash
script -f session.log
```

### Quiet Mode
To start a session in quiet mode, suppressing the usual start and stop messages:

```bash
script -q session.log
```

## Tips
- Always check the contents of the output file after ending the session to ensure everything was recorded as expected.
- Use the `-f` option if you need to monitor the session in real-time, especially during long-running commands.
- Consider using the `-a` option if you plan to record multiple sessions and want to keep a continuous log without overwriting previous data.