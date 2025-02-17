# [Linux] Bash rm 使用方式: 刪除檔案或目錄

## Overview
`rm` 命令用於刪除檔案或目錄。這是一個強大的工具，使用時需謹慎，因為刪除的檔案通常無法恢復。

## Usage
基本語法如下：
```bash
rm [options] [arguments]
```

## Common Options
- `-f`: 強制刪除檔案，無需確認。
- `-i`: 在刪除每個檔案之前提示確認。
- `-r`: 遞迴刪除目錄及其內容。
- `-v`: 顯示詳細的刪除過程。

## Common Examples
1. 刪除單個檔案：
   ```bash
   rm file.txt
   ```

2. 強制刪除檔案，不提示確認：
   ```bash
   rm -f file.txt
   ```

3. 刪除目錄及其所有內容：
   ```bash
   rm -r directory_name
   ```

4. 刪除檔案並在刪除前確認：
   ```bash
   rm -i file.txt
   ```

5. 刪除多個檔案：
   ```bash
   rm file1.txt file2.txt file3.txt
   ```

## Tips
- 在使用 `rm` 命令之前，建議先使用 `ls` 命令確認要刪除的檔案或目錄。
- 使用 `-i` 選項可以避免意外刪除重要檔案。
- 考慮使用 `trash-cli` 等工具，這樣可以將檔案移至垃圾桶，而不是永久刪除。