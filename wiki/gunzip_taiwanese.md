# [台灣] Bash gunzip 使用方法: 解壓縮.gz檔案

## Overview
`gunzip` 是一個用於解壓縮 `.gz` 格式檔案的命令。它會將壓縮的檔案還原為原始檔案，讓使用者能夠訪問和使用其中的內容。

## Usage
基本語法如下：
```
gunzip [options] [arguments]
```

## Common Options
- `-c`：將解壓縮的內容輸出到標準輸出，而不會刪除原始檔案。
- `-f`：強制解壓縮，即使檔案已經存在。
- `-k`：保留原始的壓縮檔案，解壓縮後不會刪除。
- `-v`：顯示詳細的解壓縮過程。

## Common Examples
以下是一些常見的使用範例：

1. 解壓縮單一檔案：
   ```bash
   gunzip file.gz
   ```

2. 解壓縮並保留原始檔案：
   ```bash
   gunzip -k file.gz
   ```

3. 將解壓縮的內容輸出到標準輸出：
   ```bash
   gunzip -c file.gz > output.txt
   ```

4. 解壓縮多個檔案：
   ```bash
   gunzip file1.gz file2.gz
   ```

5. 強制解壓縮已存在的檔案：
   ```bash
   gunzip -f file.gz
   ```

## Tips
- 在解壓縮之前，確保你有足夠的磁碟空間來存放解壓縮後的檔案。
- 使用 `-v` 選項可以幫助你了解解壓縮的進度和結果。
- 如果你不想刪除原始檔案，記得使用 `-k` 選項。