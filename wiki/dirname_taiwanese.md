# [Linux] Bash dirname 用法: 取得路徑的目錄部分

## Overview
`dirname` 命令用於從給定的路徑中提取出目錄部分。這對於需要獲取文件所在目錄的情況非常有用。

## Usage
基本語法如下：
```
dirname [options] [arguments]
```

## Common Options
- `-z`：當輸入的路徑為空時，返回空字符串。
- `--help`：顯示幫助信息。
- `--version`：顯示版本信息。

## Common Examples
以下是一些常見的使用範例：

1. 獲取單一文件的目錄：
   ```bash
   dirname /home/user/file.txt
   ```
   輸出：
   ```
   /home/user
   ```

2. 獲取多個文件的目錄：
   ```bash
   dirname /home/user/file1.txt /home/user/docs/file2.txt
   ```
   輸出：
   ```
   /home/user
   /home/user/docs
   ```

3. 使用變量：
   ```bash
   FILE="/home/user/file.txt"
   dirname "$FILE"
   ```
   輸出：
   ```
   /home/user
   ```

## Tips
- 使用 `dirname` 時，確保提供的路徑是有效的，否則可能會得到意外的結果。
- 可以將 `dirname` 與其他命令結合使用，例如 `basename`，以便同時獲取文件名和目錄。
- 在腳本中使用時，記得對變量進行引號處理，以避免路徑中有空格時出現錯誤。