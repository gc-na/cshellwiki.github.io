# [Linux] Bash timedatectl 用法: 管理系统时间和日期

## 概述
`timedatectl` 是一个用于查询和更改系统时间和日期的命令行工具。它可以帮助用户管理时区、同步时间以及查看当前的时间和日期设置。

## 用法
基本语法如下：
```bash
timedatectl [options] [arguments]
```

## 常用选项
- `set-time`：设置系统时间。
- `set-timezone`：设置系统时区。
- `status`：显示当前的时间和日期设置。
- `list-timezones`：列出所有可用的时区。
- `set-ntp`：启用或禁用网络时间同步。

## 常见示例
1. **查看当前时间和日期设置**
   ```bash
   timedatectl status
   ```

2. **设置系统时间**
   ```bash
   timedatectl set-time '2023-10-01 12:00:00'
   ```

3. **设置系统时区**
   ```bash
   timedatectl set-timezone Asia/Shanghai
   ```

4. **启用网络时间同步**
   ```bash
   timedatectl set-ntp true
   ```

5. **列出所有可用时区**
   ```bash
   timedatectl list-timezones
   ```

## 小贴士
- 在设置时间时，确保使用正确的格式（YYYY-MM-DD HH:MM:SS）。
- 使用 `timedatectl list-timezones` 命令可以帮助你找到合适的时区名称。
- 启用网络时间同步可以确保你的系统时间始终准确，特别是在服务器环境中。