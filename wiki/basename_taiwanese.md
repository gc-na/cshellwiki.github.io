# [Linux] Bash basename 用法: 取得檔案名稱

## Overview
`basename` 是一個用於從完整路徑中提取檔案名稱的命令。它可以幫助用戶獲取不包含路徑的檔案名稱，這在處理檔案時非常有用。

## Usage
基本語法如下：
```bash
basename [options] [arguments]
```

## Common Options
- `-a`：處理多個檔案名稱，並返回每個檔案的名稱。
- `-s`：指定要去除的後綴，這樣可以只返回檔案名稱的主要部分。

## Common Examples
以下是一些常見的使用範例：

1. 獲取單一檔案名稱：
   ```bash
   basename /usr/local/bin/script.sh
   ```
   輸出：
   ```
   script.sh
   ```

2. 獲取檔案名稱並去除特定後綴：
   ```bash
   basename /usr/local/bin/script.sh .sh
   ```
   輸出：
   ```
   script
   ```

3. 處理多個檔案名稱：
   ```bash
   basename -a /usr/local/bin/script1.sh /usr/local/bin/script2.sh
   ```
   輸出：
   ```
   script1.sh
   script2.sh
   ```

## Tips
- 使用 `basename` 時，確保提供的路徑是正確的，否則可能會得到意外的結果。
- 當需要處理多個檔案時，可以使用 `-a` 選項來一次性獲取所有檔案的名稱。
- 結合其他命令（如 `find`）使用 `basename` 可以更有效地處理檔案名稱。