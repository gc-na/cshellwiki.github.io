# [台灣] Bash hexdump 使用方式: 將檔案轉換為十六進位格式

## Overview
`hexdump` 命令用於將檔案的內容以十六進位格式顯示出來，這對於檔案的低層次分析和調試非常有用。

## Usage
基本語法如下：
```
hexdump [options] [arguments]
```

## Common Options
- `-C`：以可讀的格式顯示十六進位和 ASCII 內容。
- `-n N`：僅顯示前 N 個位元組。
- `-v`：顯示所有輸出，不省略重複的行。
- `-e FORMAT`：自定義輸出格式。

## Common Examples
以下是一些常見的用法範例：

1. 顯示檔案的十六進位內容：
   ```bash
   hexdump filename.txt
   ```

2. 以可讀格式顯示十六進位和 ASCII：
   ```bash
   hexdump -C filename.txt
   ```

3. 僅顯示檔案的前 16 個位元組：
   ```bash
   hexdump -n 16 filename.txt
   ```

4. 顯示檔案的所有內容，不省略重複行：
   ```bash
   hexdump -v filename.txt
   ```

5. 使用自定義格式輸出：
   ```bash
   hexdump -e '16/1 "%02x " "\n"' filename.txt
   ```

## Tips
- 使用 `-C` 選項可以更容易地理解輸出，因為它同時顯示十六進位和 ASCII。
- 當處理大型檔案時，使用 `-n` 選項可以幫助你快速查看檔案的開頭部分。
- 結合其他命令（例如 `grep`）使用 `hexdump` 可以進行更複雜的檔案分析。