# [台灣] Bash zip 使用法: 壓縮檔案

## Overview
`zip` 命令用於將一個或多個檔案或資料夾壓縮成一個 ZIP 檔案。這個命令不僅可以節省儲存空間，還能方便檔案的傳輸和分享。

## Usage
基本語法如下：
```bash
zip [options] [arguments]
```

## Common Options
- `-r`: 遞迴壓縮資料夾及其內容。
- `-e`: 加密壓縮檔案，要求輸入密碼。
- `-u`: 更新已存在的 ZIP 檔案，僅壓縮較新或變更過的檔案。
- `-d`: 從 ZIP 檔案中刪除檔案。

## Common Examples
1. 壓縮單個檔案：
   ```bash
   zip myfile.zip file.txt
   ```

2. 壓縮多個檔案：
   ```bash
   zip myfiles.zip file1.txt file2.txt file3.txt
   ```

3. 壓縮整個資料夾：
   ```bash
   zip -r myfolder.zip myfolder/
   ```

4. 更新已存在的 ZIP 檔案：
   ```bash
   zip -u myfiles.zip file4.txt
   ```

5. 加密 ZIP 檔案：
   ```bash
   zip -e mysecure.zip file.txt
   ```

## Tips
- 在壓縮大型資料夾時，使用 `-r` 選項可以確保所有子資料夾和檔案都被包含。
- 使用 `-e` 選項時，請選擇一個強密碼以保護您的檔案。
- 定期更新 ZIP 檔案可以幫助您保持檔案的最新狀態，避免重複壓縮相同的檔案。