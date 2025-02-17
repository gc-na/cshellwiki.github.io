# [Linux] Bash mv 用法: 移动或重命名文件和目录

## 概述
`mv` 命令用于在 Linux 和类 Unix 系统中移动或重命名文件和目录。它可以将文件从一个位置移动到另一个位置，或者更改文件的名称。

## 用法
基本语法如下：
```bash
mv [选项] [源文件或目录] [目标文件或目录]
```

## 常用选项
- `-i`：在覆盖文件之前进行确认。
- `-u`：仅在源文件比目标文件新时才移动。
- `-v`：显示详细的移动过程。
- `-f`：强制移动，不提示确认。

## 常见示例
1. **移动文件到另一个目录**
   ```bash
   mv file.txt /path/to/destination/
   ```

2. **重命名文件**
   ```bash
   mv oldname.txt newname.txt
   ```

3. **移动并覆盖文件（不提示）**
   ```bash
   mv -f file.txt /path/to/destination/
   ```

4. **移动多个文件到一个目录**
   ```bash
   mv file1.txt file2.txt /path/to/destination/
   ```

5. **使用交互模式移动文件**
   ```bash
   mv -i file.txt /path/to/destination/
   ```

## 提示
- 在使用 `mv` 命令时，确保目标路径存在，以避免错误。
- 使用 `-i` 选项可以防止意外覆盖重要文件。
- 在移动大量文件时，考虑使用 `-v` 选项来查看移动的进度。