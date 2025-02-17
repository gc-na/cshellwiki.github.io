# [Linux] Bash parted 用法: 磁盘分区管理工具

## 概述
`parted` 是一个用于管理磁盘分区的命令行工具。它可以创建、删除、调整大小和检查分区，支持多种文件系统格式。`parted` 适用于大多数 Linux 发行版，并且能够处理 GPT 和 MBR 分区表。

## 用法
基本语法如下：
```
parted [options] [arguments]
```

## 常用选项
- `-l`：列出所有可用的磁盘和分区。
- `-s`：以静默模式运行，不显示提示信息。
- `mkpart`：创建一个新分区。
- `rm`：删除指定的分区。
- `resizepart`：调整指定分区的大小。

## 常见示例
1. **列出所有磁盘和分区**
   ```bash
   parted -l
   ```

2. **创建一个新的分区**
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **删除一个分区**
   ```bash
   parted /dev/sda rm 1
   ```

4. **调整分区大小**
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

5. **检查分区**
   ```bash
   parted /dev/sda print
   ```

## 小贴士
- 在使用 `parted` 之前，建议备份重要数据，以防止意外丢失。
- 使用 `-s` 选项可以避免在脚本中出现交互提示，提高自动化处理的效率。
- 确保在操作分区时，了解每个命令的影响，尤其是在调整大小和删除分区时。