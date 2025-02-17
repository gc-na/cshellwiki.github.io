# [Linux] Bash comm 命令: 比较两个已排序文件的内容

## Overview
`comm` 命令用于比较两个已排序的文件，并输出它们的共同和不同之处。它将文件的内容分成三列：仅在第一个文件中出现的行、仅在第二个文件中出现的行，以及两个文件中都出现的行。

## Usage
基本语法如下：
```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`：抑制第一列的输出，即不显示仅在第一个文件中出现的行。
- `-2`：抑制第二列的输出，即不显示仅在第二个文件中出现的行。
- `-3`：抑制第三列的输出，即不显示两个文件中都出现的行。
- `-i`：在比较时忽略大小写。

## Common Examples
以下是一些常见的使用示例：

1. 比较两个文件并显示所有三列：
   ```bash
   comm file1.txt file2.txt
   ```

2. 仅显示在 `file1.txt` 中独有的行：
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. 仅显示在 `file2.txt` 中独有的行：
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. 忽略大小写进行比较：
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tips
- 确保输入的文件是已排序的，否则 `comm` 命令的输出将不正确。
- 可以使用 `sort` 命令对文件进行排序，例如：
  ```bash
  sort file1.txt -o file1.txt
  sort file2.txt -o file2.txt
  ```
- 使用 `-` 作为文件名可以直接从标准输入读取数据，例如：
  ```bash
  comm - file1.txt
  ```