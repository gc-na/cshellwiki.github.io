# [Linux] Bash jobs 使用方法: 管理后台作业

## Overview
`jobs` 命令用于显示当前 shell 会话中正在运行的后台作业。它可以帮助用户查看作业的状态，例如是否在运行、暂停或已停止。

## Usage
基本语法如下：
```
jobs [options] [arguments]
```

## Common Options
- `-l`：显示作业的进程ID（PID）。
- `-n`：仅显示状态发生变化的作业。
- `-p`：仅显示作业的进程ID。

## Common Examples
1. 查看所有后台作业：
   ```bash
   jobs
   ```

2. 查看包含进程ID的作业列表：
   ```bash
   jobs -l
   ```

3. 查看状态发生变化的作业：
   ```bash
   jobs -n
   ```

4. 仅显示作业的进程ID：
   ```bash
   jobs -p
   ```

## Tips
- 使用 `bg` 命令可以将暂停的作业放到后台继续运行。
- 使用 `fg` 命令可以将后台作业带回前台。
- 在使用 `jobs` 命令时，确保你在正确的 shell 会话中，以便查看相关的作业信息。