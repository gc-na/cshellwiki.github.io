# [Linux] Bash cksum 使用法: 計算檔案的校驗和

## Overview
`cksum` 命令用於計算檔案的校驗和（checksum）和字元數。它可以幫助用戶檢查檔案的完整性，確保檔案在傳輸或儲存過程中沒有損壞。

## Usage
基本語法如下：
```
cksum [options] [arguments]
```

## Common Options
- `-a, --algorithm=ALGO`：指定使用的校驗和演算法。
- `-h, --help`：顯示幫助信息。
- `-V, --version`：顯示版本信息。

## Common Examples
1. 計算單一檔案的校驗和：
   ```bash
   cksum myfile.txt
   ```

2. 計算多個檔案的校驗和：
   ```bash
   cksum file1.txt file2.txt file3.txt
   ```

3. 使用管道將輸出重定向到檔案：
   ```bash
   cksum myfile.txt > checksum.txt
   ```

4. 顯示幫助信息：
   ```bash
   cksum --help
   ```

## Tips
- 在檢查檔案完整性時，將原始檔案的校驗和與接收檔案的校驗和進行比較。
- 使用 `-a` 選項可以選擇不同的校驗和演算法，以滿足特定需求。
- 在處理大量檔案時，可以考慮將結果導出到檔案中，以便後續分析。