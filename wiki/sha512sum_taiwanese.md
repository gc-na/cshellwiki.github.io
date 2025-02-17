# [Linux] Bash sha512sum 使用法: 計算檔案的 SHA-512 雜湊值

## Overview
`sha512sum` 是一個用於計算和驗證檔案的 SHA-512 雜湊值的命令。它能夠幫助使用者確保檔案的完整性，並檢查檔案是否被修改或損壞。

## Usage
基本語法如下：
```bash
sha512sum [options] [arguments]
```

## Common Options
- `-b`：以二進位模式讀取檔案。
- `-c`：檢查檔案的 SHA-512 雜湊值是否正確。
- `-h`：顯示幫助訊息。
- `--tag`：使用標籤格式輸出雜湊值。

## Common Examples
計算單個檔案的 SHA-512 雜湊值：
```bash
sha512sum myfile.txt
```

計算多個檔案的 SHA-512 雜湊值：
```bash
sha512sum file1.txt file2.txt
```

將 SHA-512 雜湊值輸出到檔案：
```bash
sha512sum myfile.txt > myfile.sha512
```

檢查檔案的 SHA-512 雜湊值：
```bash
sha512sum -c myfile.sha512
```

## Tips
- 在檢查檔案完整性時，建議將雜湊值和檔案存放在不同的位置，以防範潛在的篡改。
- 使用 `-b` 選項可以確保以二進位模式讀取檔案，這對於某些檔案類型是必要的。
- 定期檢查重要檔案的 SHA-512 雜湊值，可以及早發現檔案的異常變更。