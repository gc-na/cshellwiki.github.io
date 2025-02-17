# [Linux] Bash md5sum 使用方法: 計算檔案的 MD5 雜湊值

## Overview
`md5sum` 命令用於計算和驗證檔案的 MD5 雜湊值。這個雜湊值可以用來檢查檔案的完整性，確保檔案在傳輸或儲存過程中未被修改。

## Usage
基本語法如下：
```
md5sum [選項] [檔案]
```

## Common Options
- `-b`：以二進位模式讀取檔案。
- `-c`：檢查檔案的 MD5 雜湊值。
- `-t`：以純文字模式讀取檔案。
- `--help`：顯示幫助信息。

## Common Examples
計算單個檔案的 MD5 雜湊值：
```bash
md5sum example.txt
```

計算多個檔案的 MD5 雜湊值：
```bash
md5sum file1.txt file2.txt
```

將 MD5 雜湊值輸出到檔案：
```bash
md5sum example.txt > example.md5
```

檢查檔案的 MD5 雜湊值：
```bash
md5sum -c example.md5
```

## Tips
- 當檔案較大時，使用 `-b` 選項可以提高計算效率。
- 為了確保檔案的完整性，建議在傳輸檔案後進行 MD5 檢查。
- 將 MD5 雜湊值儲存到檔案中，可以方便日後進行檢查。