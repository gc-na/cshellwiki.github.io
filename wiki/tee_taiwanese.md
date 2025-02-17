# [Linux] Bash tee 使用法: 將輸出同時寫入檔案和標準輸出

## Overview
`tee` 命令的主要功能是從標準輸入讀取資料，然後將這些資料寫入到標準輸出和一個或多個檔案中。這使得使用者可以在處理資料的同時，保留一份檔案的副本。

## Usage
基本語法如下：
```bash
tee [選項] [檔案...]
```

## Common Options
- `-a`：以附加模式寫入檔案，而不是覆蓋檔案。
- `-i`：忽略中斷信號。
- `-p`：在寫入檔案的同時，將輸出寫入到標準輸出。

## Common Examples
以下是一些常見的 `tee` 使用範例：

1. 將輸出寫入檔案：
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. 將輸出附加到檔案中：
   ```bash
   echo "Another line" | tee -a output.txt
   ```

3. 同時寫入多個檔案：
   ```bash
   echo "Logging data" | tee file1.txt file2.txt
   ```

4. 結合其他命令使用：
   ```bash
   ls -l | tee directory_list.txt
   ```

## Tips
- 使用 `-a` 選項可以避免覆蓋檔案，這在記錄日誌時特別有用。
- 結合管道使用 `tee` 可以方便地在多個命令之間傳遞資料。
- 確保有適當的檔案權限，否則 `tee` 可能無法寫入檔案。