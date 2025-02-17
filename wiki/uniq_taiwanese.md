# [Linux] Bash uniq 使用法: 刪除重複行

## Overview
`uniq` 命令用於刪除文本文件中的重複行。它通常與 `sort` 命令一起使用，因為 `uniq` 只會刪除相鄰的重複行。

## Usage
基本語法如下：
```
uniq [選項] [檔案]
```

## Common Options
- `-c`: 計算每一行的出現次數並顯示。
- `-d`: 只顯示重複的行。
- `-u`: 只顯示不重複的行。
- `-i`: 忽略大小寫的差異。
- `-w N`: 只比較每行的前 N 個字符。

## Common Examples
1. 刪除重複行並顯示結果：
   ```bash
   uniq input.txt output.txt
   ```

2. 計算每行出現的次數：
   ```bash
   uniq -c input.txt
   ```

3. 只顯示重複的行：
   ```bash
   uniq -d input.txt
   ```

4. 忽略大小寫的重複行：
   ```bash
   uniq -i input.txt
   ```

5. 比較前 N 個字符：
   ```bash
   uniq -w 5 input.txt
   ```

## Tips
- 在使用 `uniq` 前，建議先使用 `sort` 命令來排序文件，這樣可以確保所有重複行都是相鄰的。
- 可以使用管道將 `uniq` 與其他命令結合，例如：
  ```bash
  sort input.txt | uniq
  ```
- 當處理大文件時，考慮使用 `-o` 選項來直接將輸出寫入文件，以節省內存。