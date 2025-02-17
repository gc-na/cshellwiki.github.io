# [Linux] Bash dig Uso: DNS lookup tool

## Overview
The `dig` command, short for "Domain Information Groper," is a network administration command-line tool used for querying DNS (Domain Name System) servers. It allows users to retrieve information about various DNS records, such as A, AAAA, MX, and TXT records, making it a valuable tool for troubleshooting and verifying DNS configurations.

## Usage
The basic syntax of the `dig` command is as follows:

```bash
dig [options] [arguments]
```

## Common Options
- `@server`: Specify the DNS server to query.
- `-t type`: Specify the type of DNS record to retrieve (e.g., A, MX, TXT).
- `+short`: Provide a concise output, showing only the answer section.
- `+trace`: Trace the delegation path from the root DNS servers.
- `-x`: Perform a reverse DNS lookup.

## Common Examples

### 1. Basic DNS Query
To perform a standard DNS query for a domain:

```bash
dig example.com
```

### 2. Query Specific DNS Record Type
To query for MX (Mail Exchange) records:

```bash
dig -t MX example.com
```

### 3. Using a Specific DNS Server
To query a specific DNS server (e.g., Google's public DNS):

```bash
dig @8.8.8.8 example.com
```

### 4. Short Output
To get a brief output of the A record for a domain:

```bash
dig +short example.com
```

### 5. Reverse DNS Lookup
To find the domain associated with an IP address:

```bash
dig -x 8.8.8.8
```

### 6. Trace DNS Resolution
To trace the DNS resolution path for a domain:

```bash
dig +trace example.com
```

## Tips
- Use the `+short` option for quick results when you only need the answer.
- When troubleshooting DNS issues, the `+trace` option can help identify where the resolution fails.
- Always specify the DNS server with `@server` if you suspect issues with your default resolver.
- Familiarize yourself with different record types to make the most of `dig`'s capabilities.