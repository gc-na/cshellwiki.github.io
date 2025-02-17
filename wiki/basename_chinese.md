# [Linux] Bash basename 用法: 提取文件名

## 概述
`basename` 命令用于从给定的路径中提取文件名部分。它可以去掉路径中的目录部分，仅返回文件的名称。

## 用法
基本语法如下：
```bash
basename [options] [arguments]
```

## 常用选项
- `-a`：处理多个路径，返回每个路径的文件名。
- `-s`：指定后缀，去掉文件名中的指定后缀。

## 常见示例
1. 提取单个文件名：
   ```bash
   basename /usr/local/bin/script.sh
   ```
   输出：
   ```
   script.sh
   ```

2. 提取文件名并去掉后缀：
   ```bash
   basename /usr/local/bin/script.sh .sh
   ```
   输出：
   ```
   script
   ```

3. 处理多个路径：
   ```bash
   basename -a /usr/local/bin/script.sh /home/user/document.txt
   ```
   输出：
   ```
   script.sh
   document.txt
   ```

4. 使用自定义后缀：
   ```bash
   basename /var/log/syslog.log .log
   ```
   输出：
   ```
   syslog
   ```

## 小贴士
- 使用 `basename` 时，可以结合其他命令（如 `find`）来处理文件路径。
- 注意后缀的匹配是精确的，确保提供正确的后缀以获得预期结果。
- 对于复杂的路径处理，可以考虑使用 `dirname` 命令与 `basename` 结合使用。