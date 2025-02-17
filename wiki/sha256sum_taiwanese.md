# [Linux] Bash sha256sum 使用方法: 計算檔案的 SHA-256 雜湊值

## Overview
`sha256sum` 是一個用於計算和驗證檔案 SHA-256 雜湊值的命令。這個命令可以幫助使用者確保檔案的完整性，並檢查檔案在傳輸或儲存過程中是否被修改。

## Usage
基本語法如下：
```bash
sha256sum [options] [arguments]
```

## Common Options
- `-b`：以二進位模式讀取檔案。
- `-c`：檢查檔案的 SHA-256 雜湊值是否正確。
- `-h`：顯示幫助信息。
- `--quiet`：不輸出雜湊值，只返回狀態碼。

## Common Examples
1. 計算單個檔案的 SHA-256 雜湊值：
   ```bash
   sha256sum example.txt
   ```

2. 計算多個檔案的 SHA-256 雜湊值：
   ```bash
   sha256sum file1.txt file2.txt file3.txt
   ```

3. 將 SHA-256 雜湊值輸出到檔案中：
   ```bash
   sha256sum example.txt > hash.txt
   ```

4. 檢查檔案的 SHA-256 雜湊值：
   ```bash
   sha256sum -c hash.txt
   ```

## Tips
- 在計算雜湊值之前，確保檔案存在且可讀取。
- 使用 `-b` 選項來處理二進位檔案，以避免因為格式問題導致的錯誤。
- 定期檢查檔案的雜湊值，可以幫助你發現潛在的檔案損壞或篡改。