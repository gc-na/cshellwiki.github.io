# [Linux] Bash sysctl 用法: 查看和修改内核参数

## 概述
`sysctl` 命令用于查看和修改 Linux 内核的运行时参数。通过这个命令，用户可以动态地调整内核的行为，而无需重启系统。

## 用法
基本语法如下：
```bash
sysctl [options] [arguments]
```

## 常用选项
- `-a`：显示所有内核参数及其当前值。
- `-n`：仅显示参数的值，不显示参数名。
- `-w`：写入新的参数值。
- `-p`：从指定文件加载参数。

## 常见示例
1. 查看所有内核参数：
   ```bash
   sysctl -a
   ```

2. 查看特定参数的值，例如 `vm.swappiness`：
   ```bash
   sysctl vm.swappiness
   ```

3. 修改 `vm.swappiness` 的值为 10：
   ```bash
   sysctl -w vm.swappiness=10
   ```

4. 从文件加载参数，例如 `/etc/sysctl.conf`：
   ```bash
   sysctl -p /etc/sysctl.conf
   ```

5. 仅显示 `net.ipv4.ip_forward` 的值：
   ```bash
   sysctl -n net.ipv4.ip_forward
   ```

## 提示
- 在修改内核参数之前，建议先备份当前的配置，以防止意外情况。
- 使用 `sysctl -p` 可以快速应用在配置文件中定义的所有参数。
- 定期检查和调整内核参数可以帮助优化系统性能。