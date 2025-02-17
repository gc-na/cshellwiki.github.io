# [Linux] Bash head 用法: 顯示檔案的前幾行

## Overview
`head` 命令用來顯示檔案的前幾行內容。這在查看大型檔案的開頭部分時特別有用，讓使用者可以快速了解檔案的內容而不必打開整個檔案。

## Usage
基本語法如下：
```
head [options] [arguments]
```

## Common Options
- `-n [數字]`：指定要顯示的行數，預設為 10 行。
- `-c [數字]`：指定要顯示的字元數。
- `-q`：不顯示檔案名稱。
- `-v`：顯示檔案名稱，即使只有一個檔案。

## Common Examples
1. 顯示檔案的前 10 行（預設行數）：
   ```bash
   head filename.txt
   ```

2. 顯示檔案的前 5 行：
   ```bash
   head -n 5 filename.txt
   ```

3. 顯示檔案的前 20 個字元：
   ```bash
   head -c 20 filename.txt
   ```

4. 顯示多個檔案的前 10 行，並顯示檔案名稱：
   ```bash
   head -v file1.txt file2.txt
   ```

5. 顯示檔案的前 15 行，並隱藏檔案名稱：
   ```bash
   head -q -n 15 file1.txt file2.txt
   ```

## Tips
- 使用 `head` 可以快速檢查檔案的格式或內容，特別是在處理日誌檔案時。
- 結合其他命令使用，例如 `grep`，可以更有效地篩選出需要的資訊。
- 當處理大型檔案時，使用 `head` 可以節省時間和資源，避免開啟整個檔案。