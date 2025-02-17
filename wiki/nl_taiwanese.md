# [Linux] Bash nl 使用法: 顯示檔案行號

## Overview
`nl` 命令用於為檔案中的每一行添加行號，並可以根據需要進行格式化。這對於查看或處理文本檔案時，特別是在需要行號的情況下非常有用。

## Usage
基本語法如下：
```bash
nl [options] [arguments]
```

## Common Options
- `-b`：指定行號的格式。可以是 `a`（所有行）、`t`（只有非空行）或 `n`（不加行號）。
- `-f`：指定每個檔案的行號格式。
- `-h`：在輸出中添加標題。
- `-w`：設定行號的寬度。
- `-v`：設定行號的起始值。

## Common Examples
以下是一些常見的使用範例：

1. 為檔案添加行號：
   ```bash
   nl myfile.txt
   ```

2. 只為非空行添加行號：
   ```bash
   nl -b t myfile.txt
   ```

3. 設定行號寬度為 5：
   ```bash
   nl -w 5 myfile.txt
   ```

4. 從行號 10 開始：
   ```bash
   nl -v 10 myfile.txt
   ```

5. 為多個檔案添加行號並顯示檔案名稱：
   ```bash
   nl -h myfile1.txt myfile2.txt
   ```

## Tips
- 使用 `-w` 選項可以讓行號對齊，提升可讀性。
- 結合 `-b t` 和 `-w` 可以使輸出更整齊，特別是在處理大型檔案時。
- 可以將 `nl` 與其他命令結合使用，例如使用管道將輸出傳遞給 `less` 進行分頁顯示。