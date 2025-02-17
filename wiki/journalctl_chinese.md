# [Linux] Bash journalctl 用法: 查看系统日志

## 概述
`journalctl` 是一个用于查询和显示系统日志的命令，主要用于访问由 `systemd` 日志守护进程收集的日志信息。它可以帮助用户查看系统和服务的运行状态，诊断问题。

## 用法
基本语法如下：
```bash
journalctl [options] [arguments]
```

## 常用选项
- `-b`：显示当前启动以来的日志。
- `-f`：实时跟踪日志输出。
- `-u <unit>`：仅显示指定服务单元的日志。
- `--since <time>`：从指定时间开始显示日志。
- `--until <time>`：直到指定时间显示日志。

## 常见示例
- 查看所有日志：
  ```bash
  journalctl
  ```

- 查看当前启动以来的日志：
  ```bash
  journalctl -b
  ```

- 实时跟踪日志输出：
  ```bash
  journalctl -f
  ```

- 查看特定服务的日志，例如 `nginx`：
  ```bash
  journalctl -u nginx
  ```

- 查看从某个时间点开始的日志，例如从昨天开始：
  ```bash
  journalctl --since "yesterday"
  ```

## 提示
- 使用 `-f` 选项可以方便地监控实时日志输出，适合调试和监控服务状态。
- 可以结合 `--since` 和 `--until` 选项来查看特定时间范围内的日志，帮助定位问题。
- 定期清理日志文件，以防止占用过多磁盘空间。使用 `journalctl --vacuum-time=2weeks` 可以删除超过两周的日志。