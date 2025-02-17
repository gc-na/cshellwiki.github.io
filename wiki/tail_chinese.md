# [Linux] Bash tail 用法: 查看文件尾部内容

## 概述
`tail` 命令用于显示文件的最后几行内容。它通常用于查看日志文件的最新信息，帮助用户快速获取文件的结尾部分。

## 用法
基本语法如下：
```
tail [options] [arguments]
```

## 常用选项
- `-n [数目]`：显示文件的最后指定行数。例如，`-n 10` 显示最后 10 行。
- `-f`：实时跟踪文件的新增内容，适合查看日志文件的更新。
- `-c [字节数]`：显示文件的最后指定字节数。

## 常见示例
1. 查看文件的最后 10 行：
   ```bash
   tail filename.txt
   ```

2. 查看文件的最后 20 行：
   ```bash
   tail -n 20 filename.txt
   ```

3. 实时跟踪日志文件的更新：
   ```bash
   tail -f /var/log/syslog
   ```

4. 查看文件的最后 100 字节：
   ```bash
   tail -c 100 filename.txt
   ```

## 小贴士
- 使用 `-f` 选项时，可以按 `Ctrl + C` 停止跟踪。
- 结合 `grep` 命令可以过滤出特定内容，例如：
  ```bash
  tail -f /var/log/syslog | grep "error"
  ```
- 可以使用 `-n +[行数]` 从指定行开始显示，例如：
  ```bash
  tail -n +10 filename.txt
  ```