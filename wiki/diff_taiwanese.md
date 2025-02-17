# [Linux] Bash diff 用法: 比較檔案差異

## Overview
`diff` 命令用來比較兩個檔案的內容，並顯示它們之間的差異。這對於版本控制和檔案修改的追蹤非常有用。

## Usage
基本語法如下：
```bash
diff [選項] [檔案1] [檔案2]
```

## Common Options
- `-u`：以統一格式顯示差異，通常更易讀。
- `-i`：忽略大小寫的差異。
- `-w`：忽略所有空白字符的差異。
- `-r`：遞迴比較目錄中的檔案。

## Common Examples
比較兩個檔案的基本用法：
```bash
diff file1.txt file2.txt
```

使用統一格式顯示差異：
```bash
diff -u file1.txt file2.txt
```

忽略大小寫的差異：
```bash
diff -i file1.txt file2.txt
```

比較兩個目錄中的檔案：
```bash
diff -r dir1/ dir2/
```

## Tips
- 在使用 `diff` 時，建議使用 `-u` 選項，因為它提供的輸出格式更易於理解。
- 當需要比較多個檔案時，可以考慮使用 `diff` 的遞迴選項 `-r`，這樣可以一次性比較整個目錄。
- 如果你經常需要比較檔案，可以考慮將 `diff` 的結果導出到檔案中，使用 `>` 符號來保存輸出。