# [台灣] Bash bunzip2 使用方法: 解壓縮 bzip2 格式的檔案

## Overview
`bunzip2` 是一個用於解壓縮 bzip2 格式檔案的命令。它可以將壓縮的檔案還原為原始的未壓縮狀態，通常用於處理大型檔案以節省存儲空間。

## Usage
基本語法如下：
```
bunzip2 [選項] [檔案]
```

## Common Options
- `-k`：保留原始的壓縮檔案，解壓縮後不刪除原檔。
- `-f`：強制解壓縮，即使檔案已存在也會覆蓋。
- `-v`：顯示詳細的解壓縮過程。

## Common Examples
以下是一些常見的使用範例：

1. 解壓縮單個檔案：
   ```bash
   bunzip2 example.bz2
   ```

2. 解壓縮並保留原始檔案：
   ```bash
   bunzip2 -k example.bz2
   ```

3. 強制解壓縮已存在的檔案：
   ```bash
   bunzip2 -f example.bz2
   ```

4. 顯示解壓縮過程的詳細資訊：
   ```bash
   bunzip2 -v example.bz2
   ```

## Tips
- 在使用 `bunzip2` 解壓縮大型檔案時，建議使用 `-k` 選項以保留原始檔案，這樣可以避免資料遺失。
- 如果你不確定檔案格式，可以使用 `file` 命令來檢查檔案類型。
- 在批量解壓縮多個檔案時，可以使用通配符，例如：
  ```bash
  bunzip2 *.bz2
  ```