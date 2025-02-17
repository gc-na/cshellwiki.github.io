# [Linux] Bash rev 反轉字串: 反轉每一行的字元順序

## Overview
`rev` 命令用於反轉每一行的字元順序。這意味著，當你使用這個命令時，輸入的每一行文字都會被顛倒，從而產生一個新的輸出。

## Usage
基本語法如下：
```bash
rev [options] [arguments]
```

## Common Options
- `-s` : 只顯示反轉的字串，不顯示原始字串。
- `-h` : 顯示幫助資訊。

## Common Examples
以下是一些常見的使用範例：

1. 反轉標準輸入的字串：
   ```bash
   echo "Hello World" | rev
   ```
   輸出：
   ```
   dlroW olleH
   ```

2. 反轉檔案中的每一行：
   ```bash
   rev filename.txt
   ```
   這會將 `filename.txt` 檔案中的每一行字串反轉並顯示在終端機上。

3. 將反轉的結果輸出到新檔案：
   ```bash
   rev filename.txt > reversed.txt
   ```
   這會將反轉的內容寫入 `reversed.txt` 檔案中。

## Tips
- 使用 `rev` 時，確保你的輸入資料是以行為單位的，這樣每一行都能正確反轉。
- 可以與其他命令結合使用，例如 `cat` 或 `grep`，以處理更複雜的文本流。
- 若要快速測試，使用 `echo` 命令來檢查 `rev` 的輸出效果。