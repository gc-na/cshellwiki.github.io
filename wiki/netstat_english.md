# [Linux] Bash netstat Uso: Monitor network connections and statistics

## Overview
The `netstat` command is a powerful networking tool used to display network connections, routing tables, interface statistics, and more. It provides insights into the current network status and can help diagnose network issues.

## Usage
The basic syntax of the `netstat` command is as follows:

```bash
netstat [options] [arguments]
```

## Common Options
- `-a`: Displays all active connections and listening ports.
- `-t`: Shows TCP connections only.
- `-u`: Displays UDP connections only.
- `-n`: Shows numerical addresses instead of resolving hostnames.
- `-l`: Lists only listening sockets.
- `-p`: Displays the process ID and name associated with each connection.
- `-r`: Displays the routing table.

## Common Examples
Here are some practical examples of using the `netstat` command:

1. **Display all active connections:**
   ```bash
   netstat -a
   ```

2. **Show only TCP connections:**
   ```bash
   netstat -t
   ```

3. **List all listening ports:**
   ```bash
   netstat -l
   ```

4. **Show connections with numerical addresses:**
   ```bash
   netstat -n
   ```

5. **Display the routing table:**
   ```bash
   netstat -r
   ```

6. **Show all connections with associated process IDs:**
   ```bash
   netstat -p
   ```

## Tips
- Use `netstat -an` to quickly view all connections and their states without resolving hostnames, which can speed up the output.
- Combine options for more detailed information, such as `netstat -tuln` to see all TCP and UDP listening ports with numerical addresses.
- Regularly check your network connections with `netstat` to monitor for any unauthorized access or unusual activity.