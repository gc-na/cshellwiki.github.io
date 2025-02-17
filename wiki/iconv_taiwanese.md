# [Linux] Bash iconv 使用法: 轉換文字編碼

## Overview
`iconv` 是一個用於轉換文本文件編碼的命令行工具。它可以將文件從一種編碼格式轉換為另一種編碼格式，這在處理不同語言或系統之間的文件時特別有用。

## Usage
基本語法如下：
```
iconv [選項] [參數]
```

## Common Options
- `-f`：指定原始編碼格式。
- `-t`：指定目標編碼格式。
- `-o`：將輸出寫入指定的文件，而不是標準輸出。
- `-c`：忽略無法轉換的字符。

## Common Examples
1. 將 UTF-8 編碼的文件轉換為 ISO-8859-1：
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. 將文件從 GBK 編碼轉換為 UTF-8：
   ```bash
   iconv -f GBK -t UTF-8 input.txt -o output.txt
   ```

3. 直接在終端輸出轉換結果：
   ```bash
   iconv -f UTF-8 -t UTF-16 input.txt
   ```

4. 忽略無法轉換的字符：
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
   ```

## Tips
- 確保你知道源文件的編碼格式，這樣可以避免轉換錯誤。
- 使用 `-o` 選項可以防止覆蓋原始文件，保留備份。
- 在轉換之前，使用 `file` 命令檢查文件的編碼，以確保正確性。