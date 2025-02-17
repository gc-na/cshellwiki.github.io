# [Linux] Bash zip 用法：压缩文件和文件夹

## 概述
`zip` 命令用于将文件和文件夹压缩成一个压缩文件，通常以 `.zip` 为扩展名。它可以减小文件的大小，方便存储和传输。

## 用法
基本语法如下：
```bash
zip [选项] [压缩文件名] [要压缩的文件或文件夹]
```

## 常用选项
- `-r`：递归压缩文件夹及其内容。
- `-e`：对压缩文件进行加密。
- `-u`：更新已存在的压缩文件，添加新文件。
- `-d`：从压缩文件中删除指定文件。

## 常见示例
1. 压缩单个文件：
   ```bash
   zip myfile.zip myfile.txt
   ```

2. 压缩多个文件：
   ```bash
   zip myfiles.zip file1.txt file2.txt file3.txt
   ```

3. 递归压缩文件夹：
   ```bash
   zip -r myfolder.zip myfolder/
   ```

4. 更新压缩文件：
   ```bash
   zip -u myfiles.zip newfile.txt
   ```

5. 加密压缩文件：
   ```bash
   zip -e mysecure.zip myfile.txt
   ```

## 提示
- 在压缩大量文件时，使用 `-r` 选项可以确保所有子文件夹和文件都被包含。
- 加密压缩文件时，请确保记住密码，因为没有密码将无法解压缩。
- 定期更新压缩文件，保持文件的最新状态，可以使用 `-u` 选项。