# [Linux] Bash od 用法: 查看檔案的十六進位和其他格式

## Overview
`od`（octal dump）是一個用於顯示檔案內容的命令，通常以八進位、十六進位或ASCII格式顯示。這對於檔案的二進位數據分析特別有用。

## Usage
基本語法如下：
```
od [options] [arguments]
```

## Common Options
- `-A, --address-radix=RADIX`：指定地址的進位制，選項包括`d`（十進位）、`o`（八進位）、`x`（十六進位）。
- `-t, --format=TYPE`：指定輸出格式，例如`c`（字符）、`d`（十進位）、`x`（十六進位）。
- `-N, --read-bytes=N`：指定要讀取的字節數。
- `-v, --output-duplicates`：顯示所有輸出，包括重複的行。

## Common Examples
以下是一些常見的使用範例：

1. 顯示檔案的十六進位內容：
   ```bash
   od -x filename.txt
   ```

2. 以八進位格式顯示檔案內容：
   ```bash
   od -o filename.txt
   ```

3. 只顯示前16個字節的內容：
   ```bash
   od -N 16 filename.txt
   ```

4. 顯示檔案的ASCII字符：
   ```bash
   od -c filename.txt
   ```

5. 顯示檔案的十六進位和ASCII字符：
   ```bash
   od -A x -t x1 -t c filename.txt
   ```

## Tips
- 使用`-v`選項可以幫助你看到所有的輸出，這在檢查重複數據時特別有用。
- 結合`-N`選項可以快速檢查檔案的開頭部分，這對於大檔案的快速分析非常方便。
- 嘗試不同的格式選項來獲得不同的視圖，這有助於更好地理解檔案內容。