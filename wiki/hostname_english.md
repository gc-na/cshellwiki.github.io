# [Linux] Bash hostname Uso equivalente: Retrieve or set the system's hostname

## Overview
The `hostname` command in Bash is used to display or set the name of the current host system. The hostname is a label that identifies the device on a network, making it easier to manage and connect to different machines.

## Usage
The basic syntax of the `hostname` command is as follows:

```bash
hostname [options] [arguments]
```

## Common Options
- `-a`, `--alias`: Display the alias name of the host.
- `-d`, `--domain`: Show the domain name of the host.
- `-f`, `--fqdn`: Display the fully qualified domain name (FQDN).
- `-i`, `--ip-address`: Show the IP address associated with the hostname.
- `-s`, `--short`: Display the short hostname (without domain).
- `-V`, `--version`: Show the version of the hostname command.

## Common Examples
Here are some practical examples of using the `hostname` command:

1. **Display the current hostname:**
   ```bash
   hostname
   ```

2. **Show the fully qualified domain name (FQDN):**
   ```bash
   hostname -f
   ```

3. **Display the short hostname:**
   ```bash
   hostname -s
   ```

4. **Get the IP address of the hostname:**
   ```bash
   hostname -i
   ```

5. **Set a new hostname:**
   ```bash
   sudo hostname new-hostname
   ```

## Tips
- Always use `sudo` when changing the hostname to ensure you have the necessary permissions.
- After changing the hostname, consider updating the `/etc/hosts` file to reflect the new name for local resolution.
- Use the `hostnamectl` command on systems with `systemd` for more advanced hostname management, including setting static and transient hostnames.