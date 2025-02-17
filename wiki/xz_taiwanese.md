# [Linux] Bash xz 使用法: 壓縮和解壓縮檔案

## Overview
`xz` 是一個用於壓縮和解壓縮檔案的命令行工具，主要使用 LZMA 演算法來提供高壓縮比。它常用於減少檔案大小，特別是在需要儲存或傳輸大量數據時。

## Usage
基本語法如下：
```bash
xz [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: 解壓縮檔案。
- `-k`, `--keep`: 在壓縮或解壓縮後保留原始檔案。
- `-f`, `--force`: 強制壓縮或解壓縮，即使檔案已存在或是其他問題。
- `-z`, `--compress`: 壓縮檔案（預設行為）。
- `-9`: 使用最高壓縮比。

## Common Examples
1. 壓縮檔案：
   ```bash
   xz myfile.txt
   ```

2. 解壓縮檔案：
   ```bash
   xz -d myfile.txt.xz
   ```

3. 保留原始檔案的同時壓縮：
   ```bash
   xz -k myfile.txt
   ```

4. 使用最高壓縮比壓縮檔案：
   ```bash
   xz -9 myfile.txt
   ```

5. 解壓縮並保留原始檔案：
   ```bash
   xz -dk myfile.txt.xz
   ```

## Tips
- 在壓縮大型檔案時，考慮使用 `-9` 選項以獲得最佳壓縮效果，但這會增加處理時間。
- 使用 `-k` 選項可以在不刪除原始檔案的情況下進行壓縮，這對於需要保留原始檔案的情況特別有用。
- 定期清理不再需要的壓縮檔案，以節省磁碟空間。