# [Linux] Bash grep 用法: 查找文本中的模式

## 概述
`grep` 命令用于在文件或标准输入中搜索指定的模式，并输出包含该模式的行。它是文本处理和数据分析中非常有用的工具。

## 用法
基本语法如下：
```bash
grep [options] [arguments]
```

## 常用选项
- `-i`：忽略大小写。
- `-v`：反向匹配，输出不包含模式的行。
- `-r`：递归搜索目录中的文件。
- `-n`：显示匹配行的行号。
- `-l`：只列出包含匹配模式的文件名。

## 常见示例
1. 在文件中查找特定字符串：
   ```bash
   grep "hello" file.txt
   ```

2. 忽略大小写进行搜索：
   ```bash
   grep -i "hello" file.txt
   ```

3. 递归搜索目录中的文件：
   ```bash
   grep -r "hello" /path/to/directory
   ```

4. 显示匹配行的行号：
   ```bash
   grep -n "hello" file.txt
   ```

5. 反向匹配，输出不包含模式的行：
   ```bash
   grep -v "hello" file.txt
   ```

## 提示
- 使用 `grep -r` 时，请确保指定的目录路径正确，以避免不必要的搜索。
- 可以将多个选项组合使用，例如 `grep -rin "hello" /path/to/directory` 以递归、忽略大小写并显示行号进行搜索。
- 使用管道将 `grep` 与其他命令结合使用，可以更高效地处理数据，例如 `cat file.txt | grep "hello"`。