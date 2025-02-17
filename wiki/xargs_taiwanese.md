# [Linux] Bash xargs 使用方式: 用於處理標準輸入的命令

## Overview
`xargs` 是一個用於從標準輸入讀取數據並將其轉換為命令行參數的工具。它通常與其他命令結合使用，以便在處理大量輸入時提高效率。

## Usage
基本語法如下：
```
xargs [options] [arguments]
```

## Common Options
- `-n N`：每次傳遞 N 個參數給命令。
- `-d DELIM`：指定分隔符，默認為空格。
- `-0`：用於處理以 null 字符結尾的輸入，通常與 `find` 命令一起使用。
- `-p`：在執行每個命令之前提示用戶確認。
- `-I REPLACE_STR`：用指定的字符串替換命令中的佔位符。

## Common Examples
以下是一些常見的 `xargs` 使用範例：

1. **從 `echo` 輸出中傳遞參數**：
   ```bash
   echo "one two three" | xargs mkdir
   ```
   這會創建三個目錄：one、two 和 three。

2. **與 `find` 結合使用**：
   ```bash
   find . -name "*.txt" | xargs rm
   ```
   這會刪除當前目錄及其子目錄中的所有 `.txt` 文件。

3. **限制每次傳遞的參數數量**：
   ```bash
   echo "file1 file2 file3 file4" | xargs -n 2 cp -t /backup/
   ```
   這會每次複製兩個文件到 `/backup/` 目錄。

4. **使用 null 字符作為分隔符**：
   ```bash
   find . -name "*.jpg" -print0 | xargs -0 mv -t /images/
   ```
   這會安全地移動所有 `.jpg` 文件到 `/images/` 目錄。

## Tips
- 當處理包含空格或特殊字符的文件名時，使用 `-0` 和 `-print0` 來避免問題。
- 使用 `-n` 選項來控制每次執行的命令數量，以提高效率。
- 在執行危險操作（如刪除文件）之前，使用 `-p` 來確認操作。