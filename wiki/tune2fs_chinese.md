# [Linux] Bash tune2fs 用法: 调整 ext2/ext3/ext4 文件系统的参数

## 概述
`tune2fs` 是一个用于调整 ext2、ext3 和 ext4 文件系统参数的命令。它允许用户修改文件系统的各种设置，以优化性能或满足特定需求。

## 用法
基本语法如下：
```bash
tune2fs [选项] [参数]
```

## 常用选项
- `-c <max_mount_count>`: 设置文件系统的最大挂载次数。
- `-i <interval>`: 设置文件系统检查的时间间隔。
- `-O <feature>`: 启用或禁用特性。
- `-L <label>`: 设置文件系统的标签。
- `-e <error_behavior>`: 设置文件系统在遇到错误时的行为。

## 常见示例
1. 设置最大挂载次数为 20 次：
   ```bash
   tune2fs -c 20 /dev/sda1
   ```

2. 设置检查间隔为 30 天：
   ```bash
   tune2fs -i 30d /dev/sda1
   ```

3. 启用大文件支持特性：
   ```bash
   tune2fs -O bigalloc /dev/sda1
   ```

4. 设置文件系统标签为 "MyData":
   ```bash
   tune2fs -L MyData /dev/sda1
   ```

5. 设置在遇到错误时的行为为继续：
   ```bash
   tune2fs -e continue /dev/sda1
   ```

## 提示
- 在使用 `tune2fs` 之前，确保文件系统已卸载，以避免数据损坏。
- 使用 `tune2fs -l /dev/sda1` 命令查看当前文件系统的参数设置。
- 定期检查和调整文件系统参数，可以帮助提高系统的稳定性和性能。