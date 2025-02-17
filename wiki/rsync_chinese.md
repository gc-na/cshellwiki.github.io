# [Linux] Bash rsync 用法: 文件和目录同步工具

## 概述
`rsync` 是一个强大的文件传输和同步工具，常用于在本地和远程系统之间高效地复制和同步文件。它支持增量备份，只传输更改过的部分，从而节省带宽和时间。

## 用法
基本语法如下：
```bash
rsync [options] [source] [destination]
```

## 常用选项
- `-a`：归档模式，表示以递归方式传输文件，并保持文件的权限、时间戳等信息。
- `-v`：详细模式，输出详细的传输过程信息。
- `-z`：压缩传输，减少传输的数据量。
- `-r`：递归复制整个目录。
- `--delete`：在目标位置删除源位置中不存在的文件。
- `-e`：指定远程 shell，如 SSH。

## 常见示例
1. **基本文件同步**
   ```bash
   rsync -av /path/to/source/ /path/to/destination/
   ```
   这个命令将源目录中的所有文件和子目录同步到目标目录。

2. **通过 SSH 进行远程同步**
   ```bash
   rsync -avz -e ssh /path/to/local/ user@remote:/path/to/remote/
   ```
   这个命令将本地文件通过 SSH 同步到远程服务器。

3. **删除目标中不存在的文件**
   ```bash
   rsync -av --delete /path/to/source/ /path/to/destination/
   ```
   这个命令会确保目标目录只包含源目录中的文件，删除目标中多余的文件。

4. **压缩传输**
   ```bash
   rsync -avz /path/to/source/ /path/to/destination/
   ```
   这个命令在传输时启用压缩，以提高传输速度。

## 提示
- 在使用 `--delete` 选项时，务必小心，因为它会删除目标中不再存在于源中的文件。
- 使用 `-n` 或 `--dry-run` 选项可以先进行模拟运行，查看将要执行的操作，而不实际进行文件传输。
- 定期备份重要数据，并考虑使用 `rsync` 的定时任务（如 cron）来自动化备份过程。