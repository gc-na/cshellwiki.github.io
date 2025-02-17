# [Linux] Bash traceroute uso: Tracing network paths

## Overview
The `traceroute` command is a network diagnostic tool used to track the path that packets take from one host to another across an IP network. It helps identify the route and measure transit delays of packets across the network, which can be useful for troubleshooting connectivity issues.

## Usage
The basic syntax of the `traceroute` command is as follows:

```bash
traceroute [options] [destination]
```

## Common Options
- `-m <max_ttl>`: Set the maximum time-to-live (TTL) for the packets.
- `-n`: Show numerical addresses instead of resolving hostnames.
- `-p <port>`: Specify the destination port to use for the probe.
- `-w <timeout>`: Set the timeout for each probe in seconds.
- `-q <nqueries>`: Set the number of probe packets to send per hop.

## Common Examples
Here are several practical examples of using the `traceroute` command:

1. **Basic traceroute to a domain**:
   ```bash
   traceroute example.com
   ```

2. **Traceroute with numerical addresses**:
   ```bash
   traceroute -n example.com
   ```

3. **Traceroute specifying a maximum TTL**:
   ```bash
   traceroute -m 15 example.com
   ```

4. **Traceroute to a specific port**:
   ```bash
   traceroute -p 80 example.com
   ```

5. **Traceroute with a custom timeout**:
   ```bash
   traceroute -w 2 example.com
   ```

## Tips
- Use the `-n` option if you want faster results by avoiding DNS resolution.
- If you encounter timeouts, consider increasing the timeout value with the `-w` option.
- For troubleshooting, compare the output of `traceroute` from different locations to identify where the connectivity issues may be occurring.
- Always check your network permissions, as some networks may block traceroute packets.