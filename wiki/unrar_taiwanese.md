# [台灣] Bash unrar 使用方式: 解壓縮 RAR 檔案

## Overview
`unrar` 命令用於解壓縮 RAR 格式的檔案。這是一個非常實用的工具，可以讓使用者輕鬆地提取 RAR 檔案中的內容。

## Usage
基本語法如下：
```bash
unrar [options] [arguments]
```

## Common Options
- `e`: 解壓縮檔案到當前目錄，不保留目錄結構。
- `x`: 解壓縮檔案並保留目錄結構。
- `l`: 列出 RAR 檔案中的內容，但不解壓縮。
- `v`: 顯示詳細的解壓縮過程。
- `-o+`: 覆蓋已存在的檔案。

## Common Examples
以下是一些常見的使用範例：

1. 解壓縮到當前目錄：
   ```bash
   unrar e archive.rar
   ```

2. 解壓縮並保留目錄結構：
   ```bash
   unrar x archive.rar
   ```

3. 列出 RAR 檔案中的內容：
   ```bash
   unrar l archive.rar
   ```

4. 解壓縮並覆蓋已存在的檔案：
   ```bash
   unrar x -o+ archive.rar
   ```

## Tips
- 確保在使用 `unrar` 前已安裝該工具，通常可以透過包管理器安裝。
- 使用 `-o-` 選項可以防止覆蓋已存在的檔案，這樣可以避免意外損失資料。
- 在處理大型 RAR 檔案時，使用 `v` 選項可以幫助你了解解壓縮的進度。