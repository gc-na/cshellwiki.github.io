# [台灣] Bash grep 使用方法: 搜尋文本中的模式

## Overview
`grep` 是一個強大的命令行工具，用於在文本中搜尋特定的模式或字串。它可以從文件或標準輸入中提取符合條件的行，廣泛應用於文本處理和數據分析中。

## Usage
基本語法如下：
```
grep [選項] [參數]
```

## Common Options
- `-i`: 忽略大小寫。
- `-v`: 反向匹配，顯示不符合模式的行。
- `-r`: 遞迴搜尋子目錄中的文件。
- `-n`: 顯示匹配行的行號。
- `-c`: 顯示匹配行的計數。

## Common Examples
1. **基本搜尋**:
   ```bash
   grep "hello" file.txt
   ```
   這會在 `file.txt` 中搜尋包含 "hello" 的行。

2. **忽略大小寫**:
   ```bash
   grep -i "hello" file.txt
   ```
   這會搜尋 "hello"、"Hello"、"HELLO" 等不同大小寫的匹配。

3. **反向匹配**:
   ```bash
   grep -v "hello" file.txt
   ```
   這會顯示 `file.txt` 中不包含 "hello" 的所有行。

4. **遞迴搜尋**:
   ```bash
   grep -r "hello" /path/to/directory
   ```
   這會在指定目錄及其子目錄中搜尋 "hello"。

5. **顯示行號**:
   ```bash
   grep -n "hello" file.txt
   ```
   這會顯示 `file.txt` 中包含 "hello" 的行及其行號。

## Tips
- 使用 `-r` 選項時，確保你在正確的目錄中，以免搜尋過多不必要的文件。
- 結合其他命令使用，例如 `cat` 或 `find`，可以提高效率。
- 使用正則表達式時，`grep` 提供了強大的模式匹配能力，善加利用可以達到更精確的搜尋結果。