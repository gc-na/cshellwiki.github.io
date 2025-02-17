# [Linux] Bash udevadm Uso: Manage device events and properties

## Overview
The `udevadm` command is a tool used to manage the udev device manager in Linux. It allows users to monitor and control device events, query device properties, and manage the udev database. This command is essential for system administrators and developers who need to interact with hardware devices and their configurations.

## Usage
The basic syntax of the `udevadm` command is as follows:

```bash
udevadm [options] [arguments]
```

## Common Options
- `info`: Display information about a device.
- `monitor`: Monitor udev events in real-time.
- `trigger`: Trigger events for devices.
- `settle`: Wait for all udev events to be processed.
- `control`: Control the udev daemon, such as starting or stopping it.

## Common Examples

### Display Information About a Device
To get detailed information about a specific device, use the `info` option followed by the device path:

```bash
udevadm info --query=all --name=/dev/sda
```

### Monitor Real-Time Device Events
To observe device events as they occur, use the `monitor` option:

```bash
udevadm monitor
```

### Trigger Events for Devices
You can trigger events for all devices or a specific device with the `trigger` option:

```bash
udevadm trigger
```

### Wait for All udev Events to Settle
To ensure that all udev events have been processed, use the `settle` option:

```bash
udevadm settle
```

### Control the udev Daemon
To stop the udev daemon, you can use the `control` option:

```bash
udevadm control --stop
```

## Tips
- Always use the `info` option to verify device properties before making changes.
- Use `monitor` in a separate terminal to observe events while performing actions that affect devices.
- Be cautious when using `trigger` as it can cause devices to be re-enumerated, which may disrupt ongoing processes.
- Regularly check the udev rules in `/etc/udev/rules.d/` to customize device handling according to your needs.