# [Linux] Bash rmdir 用法: 删除空目录

## 概述
`rmdir` 命令用于删除空目录。如果目录中包含文件或其他目录，`rmdir` 将无法删除该目录。

## 用法
基本语法如下：
```
rmdir [选项] [参数]
```

## 常用选项
- `-p`：递归删除目录及其父目录（如果父目录为空）。
- `--ignore-fail-on-non-empty`：忽略非空目录的错误，不会显示错误信息。

## 常见示例
1. 删除一个空目录：
   ```bash
   rmdir my_empty_directory
   ```

2. 递归删除一个空目录及其父目录：
   ```bash
   rmdir -p my_empty_directory/parent_directory
   ```

3. 忽略非空目录的错误：
   ```bash
   rmdir --ignore-fail-on-non-empty my_non_empty_directory
   ```

## 提示
- 在使用 `rmdir` 前，确保目录是空的，可以使用 `ls` 命令查看目录内容。
- 使用 `-p` 选项时，确保父目录也为空，否则将无法删除。
- 如果需要删除非空目录，请考虑使用 `rm -r` 命令，但要小心使用，以免误删重要文件。