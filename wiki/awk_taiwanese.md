# [台灣] Bash awk 用法: 文本處理工具

## Overview
`awk` 是一個強大的文本處理工具，主要用於模式匹配和報告生成。它可以從文本文件或標準輸入中提取和處理數據，特別適合處理結構化的數據，如 CSV 文件。

## Usage
基本語法如下：
```bash
awk [options] [arguments]
```

## Common Options
- `-F` : 指定字段分隔符，例如 `-F,` 用於 CSV 文件。
- `-v` : 定義變數，例如 `-v var=value`。
- `-f` : 從文件中讀取 awk 程序。
- `-e` : 直接在命令行中寫 awk 程序。

## Common Examples
1. **打印文件的第一列**
   ```bash
   awk '{print $1}' filename.txt
   ```

2. **使用逗號作為分隔符，打印第二列**
   ```bash
   awk -F, '{print $2}' data.csv
   ```

3. **計算文件中數字的總和**
   ```bash
   awk '{sum += $1} END {print sum}' numbers.txt
   ```

4. **篩選出大於 100 的行**
   ```bash
   awk '$1 > 100' data.txt
   ```

5. **使用變數來計算平均值**
   ```bash
   awk -v total=0 '{total += $1} END {print total/NR}' numbers.txt
   ```

## Tips
- 使用 `-F` 選項來處理不同的分隔符，這樣可以適應多種數據格式。
- 在處理大型文件時，考慮使用 `awk` 的內建變數如 `NR`（行號）和 `NF`（字段數）來提高效率。
- 結合 `awk` 與其他命令（如 `grep` 或 `sort`）可以進一步增強數據處理能力。