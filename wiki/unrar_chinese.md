# [Linux] Bash unrar 用法: 解压RAR文件

## 概述
`unrar` 命令用于解压缩 RAR 格式的压缩文件。它可以提取文件和目录，方便用户访问压缩包中的内容。

## 用法
基本语法如下：
```bash
unrar [options] [arguments]
```

## 常用选项
- `e`：提取文件到当前目录，不保留目录结构。
- `x`：提取文件到指定目录，保留目录结构。
- `l`：列出压缩包中的文件，但不提取。
- `t`：测试压缩包的完整性。
- `v`：详细模式，显示提取过程中的详细信息。

## 常见示例
1. 提取当前目录下的 RAR 文件：
   ```bash
   unrar e example.rar
   ```

2. 提取 RAR 文件到指定目录，并保留目录结构：
   ```bash
   unrar x example.rar /path/to/destination/
   ```

3. 列出 RAR 文件中的内容：
   ```bash
   unrar l example.rar
   ```

4. 测试 RAR 文件的完整性：
   ```bash
   unrar t example.rar
   ```

5. 以详细模式提取文件：
   ```bash
   unrar v x example.rar
   ```

## 提示
- 确保你有权限访问和写入目标目录。
- 使用 `-o+` 选项可以在提取时自动覆盖已有文件。
- 如果需要查看帮助信息，可以使用 `unrar` 命令不带任何参数。