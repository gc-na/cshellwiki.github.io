# [Linux] Bash comm 用法: 比較兩個已排序的檔案

## Overview
`comm` 命令用於比較兩個已排序的檔案，並輸出它們之間的差異。這個命令會將檔案的內容分為三個部分：僅在第一個檔案中出現的行、僅在第二個檔案中出現的行，以及兩個檔案中都出現的行。

## Usage
基本語法如下：
```
comm [選項] [檔案1] [檔案2]
```

## Common Options
- `-1`：不顯示僅在檔案1中的行。
- `-2`：不顯示僅在檔案2中的行。
- `-3`：不顯示在兩個檔案中都出現的行。
- `-i`：忽略大小寫的差異。
- `-u`：只顯示唯一的行。

## Common Examples
1. 比較兩個檔案並顯示所有差異：
   ```bash
   comm file1.txt file2.txt
   ```

2. 僅顯示在 `file1.txt` 中的行：
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. 僅顯示在 `file2.txt` 中的行：
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. 忽略大小寫進行比較：
   ```bash
   comm -i file1.txt file2.txt
   ```

5. 顯示唯一的行：
   ```bash
   comm -u file1.txt file2.txt
   ```

## Tips
- 確保比較的檔案已經排序，因為 `comm` 需要已排序的輸入。
- 使用 `sort` 命令可以輕鬆地對檔案進行排序，例如：
  ```bash
  sort file1.txt -o file1.txt
  sort file2.txt -o file2.txt
  ```
- 當處理大型檔案時，考慮使用 `-o` 選項將輸出重定向到檔案中，以便後續分析。