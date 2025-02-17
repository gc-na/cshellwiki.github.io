# [台灣] Bash sort 使用法: 排序檔案內容

## Overview
`sort` 命令用於將檔案中的行進行排序。它可以根據字母順序、數字大小或其他自定義條件來排列資料，並且可以處理標準輸入和檔案輸出。

## Usage
基本語法如下：
```
sort [選項] [檔案]
```

## Common Options
- `-r`：反向排序，從大到小。
- `-n`：按數字排序，而不是字母。
- `-k`：指定排序的欄位。
- `-u`：僅顯示唯一的行。
- `-o`：將結果輸出到指定檔案。

## Common Examples
1. 按字母順序排序檔案內容：
   ```bash
   sort filename.txt
   ```

2. 反向排序檔案內容：
   ```bash
   sort -r filename.txt
   ```

3. 按數字排序：
   ```bash
   sort -n numbers.txt
   ```

4. 指定排序的欄位（例如，第二欄）：
   ```bash
   sort -k 2 filename.txt
   ```

5. 將排序結果輸出到新檔案：
   ```bash
   sort filename.txt -o sorted.txt
   ```

## Tips
- 使用 `-u` 選項可以快速去除重複的行，這對於清理資料非常有用。
- 在處理大型檔案時，考慮使用 `-S` 選項來指定可用的記憶體大小，以提高性能。
- 結合 `-k` 和 `-n` 可以實現更複雜的排序需求，例如先按數字排序，再按字母排序。