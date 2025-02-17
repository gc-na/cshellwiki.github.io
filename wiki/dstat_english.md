# [Linux] Bash dstat Uso equivalente: Monitor system resources in real-time

## Overview
The `dstat` command is a versatile tool for monitoring system resources in real-time. It provides a comprehensive overview of various system metrics, including CPU usage, memory consumption, disk activity, and network statistics. This makes it an essential utility for system administrators and developers who need to analyze system performance and troubleshoot issues.

## Usage
The basic syntax of the `dstat` command is as follows:

```bash
dstat [options] [arguments]
```

## Common Options
- `-c`: Show CPU statistics.
- `-d`: Display disk statistics.
- `-n`: Show network statistics.
- `-m`: Display memory statistics.
- `-t`: Include a timestamp in the output.
- `--help`: Show help information and available options.

## Common Examples

### Monitor CPU and Memory Usage
To monitor CPU and memory usage in real-time, you can use:

```bash
dstat -c -m
```

### Monitor Disk and Network Activity
To see disk and network activity, you can run:

```bash
dstat -d -n
```

### Comprehensive Resource Monitoring
For a complete overview of system resources, use:

```bash
dstat -cdnm
```

### Include Timestamps
If you want to include timestamps in your output, you can add the `-t` option:

```bash
dstat -cdnmt
```

## Tips
- Combine options to tailor the output to your needs; for example, `dstat -cdnm` gives a broad view of system performance.
- Use `dstat --help` to explore all available options and customize your monitoring.
- Consider running `dstat` in a screen session or redirecting output to a file for long-term monitoring.