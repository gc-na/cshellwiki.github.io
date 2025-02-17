# [Linux] Bash wc 用法: 計算文件的行數、字數和字元數

## Overview
`wc`（word count）是一個用於計算文件中行數、字數和字元數的命令。這個命令非常有用，特別是在處理文本文件時，可以快速獲得文件的基本統計信息。

## Usage
基本語法如下：
```
wc [options] [arguments]
```

## Common Options
- `-l`: 計算行數。
- `-w`: 計算字數。
- `-c`: 計算字元數。
- `-m`: 計算字元數（包括多字節字符）。
- `-L`: 顯示文件中最長行的長度。

## Common Examples
1. **計算行數**
   ```bash
   wc -l filename.txt
   ```

2. **計算字數**
   ```bash
   wc -w filename.txt
   ```

3. **計算字元數**
   ```bash
   wc -c filename.txt
   ```

4. **同時計算行數、字數和字元數**
   ```bash
   wc filename.txt
   ```

5. **計算多個文件的行數、字數和字元數**
   ```bash
   wc file1.txt file2.txt
   ```

6. **顯示最長行的長度**
   ```bash
   wc -L filename.txt
   ```

## Tips
- 使用 `wc` 時，可以將其與其他命令結合使用，例如使用管道（`|`）來計算命令輸出的行數或字數。
- 若要獲得更詳細的統計信息，可以結合 `grep` 和 `wc`，例如計算特定模式的行數。
- 在處理大型文件時，考慮使用 `-l` 或 `-w` 來快速獲得所需的信息，而不是查看整個文件。