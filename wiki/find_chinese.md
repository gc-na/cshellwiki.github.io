# [Linux] Bash find 用法: 查找文件名

## 概述
`find` 命令用于在文件系统中查找符合特定条件的文件和目录。它可以根据名称、类型、大小、修改时间等多种标准进行搜索。

## 用法
基本语法如下：
```
find [选项] [参数]
```

## 常用选项
- `-name`：根据文件名查找。
- `-type`：根据文件类型查找（如 f 表示文件，d 表示目录）。
- `-size`：根据文件大小查找。
- `-mtime`：根据文件的修改时间查找。
- `-exec`：对找到的文件执行指定命令。

## 常见示例
1. 根据文件名查找：
   ```bash
   find /path/to/search -name "filename.txt"
   ```

2. 查找所有的目录：
   ```bash
   find /path/to/search -type d
   ```

3. 查找大于 1MB 的文件：
   ```bash
   find /path/to/search -size +1M
   ```

4. 查找最近 7 天内修改过的文件：
   ```bash
   find /path/to/search -mtime -7
   ```

5. 对找到的文件执行命令（例如删除）：
   ```bash
   find /path/to/search -name "*.tmp" -exec rm {} \;
   ```

## 小贴士
- 使用 `-iname` 选项可以进行不区分大小写的搜索。
- 可以使用 `-print` 选项来显示找到的文件，尽管这是默认行为。
- 在使用 `-exec` 时，确保在命令末尾加上 `\;` 以结束命令。
- 为了提高效率，可以在搜索时限制搜索的深度，例如使用 `-maxdepth` 选项。