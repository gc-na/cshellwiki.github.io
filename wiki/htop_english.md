# [Linux] Bash htop Uso: Monitoramento interativo de processos

## Overview
The `htop` command is an interactive process viewer for Unix systems. It provides a real-time, user-friendly interface to monitor system processes, CPU usage, memory consumption, and other system metrics. Unlike the traditional `top` command, `htop` allows users to scroll through the process list and manage processes more easily.

## Usage
The basic syntax of the `htop` command is as follows:

```bash
htop [options] [arguments]
```

## Common Options
- `-h`, `--help`: Display help information about `htop`.
- `-s`, `--sort`: Sort the process list by a specified column (e.g., CPU, memory).
- `-p`, `--pid`: Monitor specific process IDs.
- `-C`, `--no-color`: Run `htop` without color output.
- `-d`, `--delay`: Set the delay between updates in tenths of seconds.

## Common Examples
- Launch `htop` to view all processes:
    ```bash
    htop
    ```

- Launch `htop` with a specific delay of 2 seconds between updates:
    ```bash
    htop -d 20
    ```

- Sort processes by memory usage:
    ```bash
    htop -s MEM
    ```

- Monitor specific process IDs (e.g., 1234 and 5678):
    ```bash
    htop -p 1234,5678
    ```

- Run `htop` without color output:
    ```bash
    htop -C
    ```

## Tips
- Use the arrow keys to navigate through the process list and the F1-F10 function keys for various actions.
- Press `F9` to kill a selected process and choose a signal to send.
- Customize the display by pressing `F2` to access the setup menu, where you can adjust the display options and sorting preferences.
- To search for a specific process, press `F3` and type the name or part of the name of the process you are looking for.