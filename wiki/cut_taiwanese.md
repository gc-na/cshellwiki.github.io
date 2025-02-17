# [Linux] Bash cut 使用方式: 切割文本行

## Overview
`cut` 命令用於從文本行中提取特定的字段或字符，通常用於處理文本文件或命令輸出的數據。這個命令非常適合在處理結構化數據時使用，例如 CSV 文件。

## Usage
基本語法如下：
```
cut [options] [arguments]
```

## Common Options
- `-f`：指定要提取的字段，通常與 `-d` 選項一起使用。
- `-d`：定義字段分隔符，預設為制表符。
- `-c`：指定要提取的字符範圍。
- `--complement`：提取不在指定範圍內的字段或字符。

## Common Examples
1. 提取以逗號分隔的第二個字段：
   ```bash
   cut -d ',' -f 2 filename.txt
   ```

2. 提取特定字符範圍（例如第1到第5個字符）：
   ```bash
   cut -c 1-5 filename.txt
   ```

3. 從標準輸入中提取字段：
   ```bash
   echo "apple,banana,cherry" | cut -d ',' -f 1
   ```

4. 提取不在指定字段範圍內的字段（例如提取第2和第3個字段以外的所有字段）：
   ```bash
   cut -d ',' -f 2,3 --complement filename.txt
   ```

## Tips
- 當處理以空格或其他字符分隔的文件時，記得使用 `-d` 來指定正確的分隔符。
- 使用 `-c` 時，確保字符範圍不超過行的長度，否則將不會返回任何結果。
- 可以將 `cut` 與其他命令（如 `grep` 或 `sort`）結合使用，以進一步處理數據。