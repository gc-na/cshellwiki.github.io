# [Linux] Bash ping6 Uso: Testar conectividade de rede IPv6

## Overview
The `ping6` command is a network utility used to test the reachability of a host on an Internet Protocol version 6 (IPv6) network. It sends Internet Control Message Protocol (ICMP) Echo Request messages to the specified address and waits for Echo Reply messages, helping to diagnose network connectivity issues.

## Usage
The basic syntax of the `ping6` command is as follows:

```bash
ping6 [options] [arguments]
```

## Common Options
- `-c <count>`: Specifies the number of packets to send.
- `-i <interval>`: Sets the interval in seconds between sending each packet.
- `-s <size>`: Defines the number of data bytes to be sent.
- `-W <timeout>`: Sets the timeout in seconds for waiting for a response.

## Common Examples

1. **Ping a specific IPv6 address:**
   ```bash
   ping6 2001:db8::1
   ```

2. **Ping a host with a specific number of packets:**
   ```bash
   ping6 -c 5 google.com
   ```

3. **Ping a host with a custom packet size:**
   ```bash
   ping6 -s 1280 2001:db8::1
   ```

4. **Ping a host with a specified interval:**
   ```bash
   ping6 -i 2 google.com
   ```

5. **Ping a host and set a timeout for responses:**
   ```bash
   ping6 -W 2 2001:db8::1
   ```

## Tips
- Use the `-c` option to limit the number of packets sent, which can be useful for quick tests.
- The `-i` option can help reduce network congestion by controlling the rate of packets sent.
- Always check your network configuration if you are unable to reach a host, as it may not be a problem with the command itself.