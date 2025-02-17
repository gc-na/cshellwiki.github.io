# [Linux] Bash tac 用法: 反向顯示檔案內容

## Overview
`tac` 是一個用於顯示檔案內容的命令，與 `cat` 相對，它會將檔案的內容反向顯示。這意味著它會從檔案的最後一行開始顯示，直到第一行結束。

## Usage
基本語法如下：
```bash
tac [選項] [檔案]
```

## Common Options
- `-r`：使用正則表達式來分隔行。
- `-s`：指定行的分隔符，預設為換行符。
- `-b`：在每行的結尾添加空白行。

## Common Examples
以下是一些常見的使用範例：

1. 反向顯示檔案內容：
   ```bash
   tac example.txt
   ```

2. 使用自訂的行分隔符：
   ```bash
   tac -s ',' example.csv
   ```

3. 反向顯示多個檔案的內容：
   ```bash
   tac file1.txt file2.txt
   ```

4. 將反向顯示的內容輸出到新檔案：
   ```bash
   tac example.txt > reversed_example.txt
   ```

## Tips
- 當需要快速查看檔案的最後幾行時，`tac` 是一個非常方便的工具。
- 結合 `grep` 使用，可以快速找到特定模式的最後出現行：
  ```bash
  tac example.txt | grep 'pattern'
  ```
- 使用 `less` 或 `more` 命令來分頁顯示長檔案的反向內容：
  ```bash
  tac example.txt | less
  ```