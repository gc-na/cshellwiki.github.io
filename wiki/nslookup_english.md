# [Linux] Bash nslookup Uso: Query DNS records

## Overview
The `nslookup` command is a network utility used to query the Domain Name System (DNS) to obtain domain name or IP address mapping information. It helps users troubleshoot DNS issues by allowing them to look up DNS records for a specific domain or IP address.

## Usage
The basic syntax of the `nslookup` command is as follows:

```bash
nslookup [options] [arguments]
```

## Common Options
- `-type=TYPE`: Specifies the type of DNS record to query (e.g., A, AAAA, MX, TXT).
- `-timeout=SECONDS`: Sets the time to wait for a response before timing out.
- `-retry=NUM`: Specifies the number of retries for a query.
- `-debug`: Enables debugging mode for more detailed output.

## Common Examples
Here are some practical examples of using the `nslookup` command:

### 1. Querying an A Record
To find the IP address associated with a domain name:

```bash
nslookup example.com
```

### 2. Querying a Specific DNS Record Type
To look up the MX (Mail Exchange) records for a domain:

```bash
nslookup -type=MX example.com
```

### 3. Specifying a DNS Server
To query a specific DNS server (e.g., Google's public DNS):

```bash
nslookup example.com 8.8.8.8
```

### 4. Using Debug Mode
To enable debug mode for detailed output:

```bash
nslookup -debug example.com
```

## Tips
- Use `nslookup` with different record types to gather comprehensive information about a domain.
- If you encounter issues, try querying different DNS servers to see if the problem persists.
- Familiarize yourself with common DNS record types to make the most out of `nslookup`.