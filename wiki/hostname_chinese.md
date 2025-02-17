# [Linux] Bash hostname 用法: 显示或设置主机名

## 概述
`hostname` 命令用于显示或设置系统的主机名。主机名是计算机在网络中的标识，可以是简单的名称或完全合格的域名（FQDN）。

## 用法
基本语法如下：
```
hostname [options] [arguments]
```

## 常用选项
- `-a`：显示别名。
- `-d`：显示域名。
- `-f`：显示完全合格的域名。
- `-i`：显示主机的IP地址。
- `-s`：显示短主机名。

## 常见示例
1. 显示当前主机名：
   ```bash
   hostname
   ```

2. 显示完全合格的域名：
   ```bash
   hostname -f
   ```

3. 显示主机的IP地址：
   ```bash
   hostname -i
   ```

4. 设置新的主机名：
   ```bash
   sudo hostname new-hostname
   ```

5. 显示主机的别名：
   ```bash
   hostname -a
   ```

## 提示
- 修改主机名后，建议重启系统以确保所有服务都能识别新的主机名。
- 使用 `hostnamectl` 命令可以更方便地管理主机名（在系统使用systemd的情况下）。
- 确保新的主机名在网络中是唯一的，以避免冲突。