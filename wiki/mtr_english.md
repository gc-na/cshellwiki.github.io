# [Linux] Bash mtr Uso: Network diagnostic tool

## Overview
The `mtr` command, short for "My Traceroute," is a network diagnostic tool that combines the functionality of the `ping` and `traceroute` commands. It provides real-time information about the route packets take to reach a destination, along with statistics on packet loss and latency for each hop along the way.

## Usage
The basic syntax of the `mtr` command is as follows:

```bash
mtr [options] [destination]
```

## Common Options
- `-r`: Run in report mode, which provides a summary of the results and exits.
- `-c <count>`: Specify the number of pings to send (default is infinite).
- `-i <interval>`: Set the interval between pings in seconds (default is 1 second).
- `-p`: Enable the use of a specific port for the probe.
- `-w`: Use wide output format for better readability.

## Common Examples

### Basic Usage
To run `mtr` to a specific destination, simply type:

```bash
mtr example.com
```

### Report Mode
To generate a report and exit after a certain number of pings, use:

```bash
mtr -r -c 10 example.com
```

### Custom Interval
To set a custom interval of 2 seconds between pings:

```bash
mtr -i 2 example.com
```

### Using a Specific Port
To probe a specific port (e.g., 80 for HTTP):

```bash
mtr -p 80 example.com
```

### Wide Output Format
For better readability, especially with many hops:

```bash
mtr -w example.com
```

## Tips
- Use `mtr` with the `-r` option for a quick summary of network performance.
- Combine options to tailor the output to your needs, such as using `-c` with `-i` for controlled testing.
- Regularly monitor your network with `mtr` to identify potential issues before they escalate.