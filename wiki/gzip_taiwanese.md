# [Linux] Bash gzip 使用法: 壓縮和解壓縮檔案

## Overview
`gzip` 是一個用於壓縮和解壓縮檔案的命令行工具。它使用 DEFLATE 演算法來減少檔案的大小，特別適合文本檔案。

## Usage
基本語法如下：
```bash
gzip [options] [arguments]
```

## Common Options
- `-d` 或 `--decompress`: 解壓縮檔案。
- `-k` 或 `--keep`: 壓縮檔案時保留原始檔案。
- `-v` 或 `--verbose`: 顯示詳細的壓縮過程。
- `-r` 或 `--recursive`: 遞歸壓縮目錄中的所有檔案。

## Common Examples
壓縮檔案：
```bash
gzip filename.txt
```

解壓縮檔案：
```bash
gzip -d filename.txt.gz
```

保留原始檔案的壓縮：
```bash
gzip -k filename.txt
```

遞歸壓縮目錄中的所有檔案：
```bash
gzip -r directory_name/
```

顯示詳細的壓縮過程：
```bash
gzip -v filename.txt
```

## Tips
- 使用 `-k` 選項可以在壓縮後保留原始檔案，這樣可以避免意外刪除重要檔案。
- 對於大型檔案，考慮使用 `-9` 選項來獲得最佳壓縮率，但這會增加壓縮時間。
- 定期檢查壓縮檔案的完整性，確保資料未損壞。