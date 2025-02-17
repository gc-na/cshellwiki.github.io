# [Linux] Bash expand 使用法: 將制表符轉換為空格

## Overview
`expand` 命令用於將文本文件中的制表符（Tab）轉換為空格。這在需要保持文本格式一致性時非常有用，特別是在不同的編輯器或環境中查看文件時。

## Usage
基本語法如下：
```
expand [選項] [參數]
```

## Common Options
- `-t, --tabs=N`：設置每個制表符的空格數，預設為 8。
- `-i`：僅轉換行首的制表符。
- `-f`：將制表符轉換為空格，並在行首保留制表符。

## Common Examples
1. 將文件中的制表符轉換為預設的空格數（8個空格）：
   ```bash
   expand filename.txt
   ```

2. 指定每個制表符轉換為 4 個空格：
   ```bash
   expand -t 4 filename.txt
   ```

3. 僅轉換行首的制表符：
   ```bash
   expand -i filename.txt
   ```

4. 將結果輸出到新文件中：
   ```bash
   expand filename.txt > newfile.txt
   ```

## Tips
- 在處理大型文件時，可以考慮使用 `-o` 選項來指定輸出格式，這樣可以更靈活地控制轉換結果。
- 使用 `cat -A` 命令來檢查文件中的制表符和空格，這樣可以更清楚地了解轉換的效果。
- 在編輯器中查看轉換後的文件，以確保格式符合預期，特別是在不同的環境中。