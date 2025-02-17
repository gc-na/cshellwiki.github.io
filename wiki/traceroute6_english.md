# [Linux] Bash traceroute6 Usage: Trace IPv6 Network Paths

## Overview
The `traceroute6` command is a network diagnostic tool used to trace the path that packets take from your machine to a specified destination over an IPv6 network. It helps in identifying the route and measuring transit delays of packets across the network.

## Usage
The basic syntax of the `traceroute6` command is as follows:

```bash
traceroute6 [options] [destination]
```

## Common Options
- `-m <max_ttl>`: Set the maximum time-to-live (TTL) for the packets.
- `-p <port>`: Specify the destination port number to use.
- `-q <nqueries>`: Set the number of probe packets to send per hop.
- `-w <waittime>`: Define the time to wait for a response before timing out.

## Common Examples

1. **Basic Traceroute to a Host**
   ```bash
   traceroute6 google.com
   ```

2. **Setting Maximum TTL**
   ```bash
   traceroute6 -m 30 google.com
   ```

3. **Specifying a Port Number**
   ```bash
   traceroute6 -p 80 google.com
   ```

4. **Sending Multiple Probes per Hop**
   ```bash
   traceroute6 -q 5 google.com
   ```

5. **Setting a Timeout for Responses**
   ```bash
   traceroute6 -w 2 google.com
   ```

## Tips
- Always ensure that your network supports IPv6 before using `traceroute6`, as it is specifically designed for IPv6 addresses.
- Use the `-m` option to prevent the command from running indefinitely by limiting the number of hops.
- Combine options to customize your traceroute command for specific needs, such as adjusting the number of queries or setting a timeout for responses.