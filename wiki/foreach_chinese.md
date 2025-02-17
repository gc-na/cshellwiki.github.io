# [Linux] Bash foreach 用法: 批量处理命令

## 概述
`foreach` 命令用于在 Bash 脚本中对一组项目执行相同的命令。它可以简化对多个文件或数据的处理，使得批量操作变得更加高效。

## 用法
基本语法如下：
```bash
foreach variable (list)
    command
end
```

## 常用选项
- `variable`：用于存储当前处理的项目。
- `list`：要处理的项目列表，可以是文件名、字符串等。
- `command`：要对每个项目执行的命令。

## 常见示例
以下是一些常见的 `foreach` 使用示例：

### 示例 1: 遍历文件列表
```bash
foreach file (file1.txt file2.txt file3.txt)
    echo "Processing $file"
end
```

### 示例 2: 批量重命名文件
```bash
foreach file (oldname*.txt)
    mv $file ${file/oldname/newname}
end
```

### 示例 3: 对多个目录执行相同的操作
```bash
foreach dir (dir1 dir2 dir3)
    cd $dir
    ls -l
    cd ..
end
```

## 小贴士
- 确保在使用 `foreach` 时，列表中的项目是正确的，以避免不必要的错误。
- 使用 `echo` 命令进行调试，可以帮助你确认每个项目的处理情况。
- 在处理大量文件时，考虑使用 `find` 命令结合 `xargs`，以提高效率。