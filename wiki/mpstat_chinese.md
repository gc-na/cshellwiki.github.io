# [Linux] Bash mpstat 使用说明: 显示 CPU 使用情况

## 概述
mpstat 命令用于报告各个 CPU 的使用情况。它可以帮助用户监控系统的 CPU 性能，识别潜在的瓶颈，并进行性能调优。

## 用法
mpstat 的基本语法如下：

```bash
mpstat [options] [arguments]
```

## 常用选项
- `-P ALL`：显示所有 CPU 的统计信息。
- `-u`：显示 CPU 使用情况的百分比。
- `-h`：以人类可读的格式显示输出。
- `-o`：将输出保存到文件中。
- `interval`：指定更新的时间间隔（以秒为单位）。
- `count`：指定要报告的次数。

## 常见示例
1. 显示所有 CPU 的使用情况：

   ```bash
   mpstat -P ALL
   ```

2. 每 2 秒更新一次 CPU 使用情况，报告 5 次：

   ```bash
   mpstat 2 5
   ```

3. 以人类可读的格式显示 CPU 使用情况：

   ```bash
   mpstat -h
   ```

4. 将输出保存到文件中：

   ```bash
   mpstat -o CSV 1 10 > cpu_usage.csv
   ```

## 提示
- 定期监控 CPU 使用情况可以帮助及时发现性能问题。
- 使用 `-P ALL` 选项可以更全面地了解多核 CPU 的性能。
- 将输出保存到文件中可以方便后续分析和记录。