# [台灣] Bash sed 用法: 文本替換與處理工具

## Overview
`sed` 是一個流編輯器，用於對文本進行非互動式的處理和變更。它可以用來替換、刪除、插入或轉換文本行，常用於自動化文本處理任務。

## Usage
基本語法如下：
```bash
sed [options] [arguments]
```

## Common Options
- `-e`: 指定要執行的編輯命令。
- `-i`: 直接在文件中進行修改，而不是輸出到標準輸出。
- `-n`: 抑制自動輸出，僅在使用 `p` 命令時輸出。
- `s`: 替換命令，用於替換文本。

## Common Examples
1. **替換文本**
   將文件中的 "apple" 替換為 "orange"：
   ```bash
   sed 's/apple/orange/g' filename.txt
   ```

2. **直接修改文件**
   在文件中直接替換 "apple" 為 "orange"：
   ```bash
   sed -i 's/apple/orange/g' filename.txt
   ```

3. **刪除行**
   刪除包含 "delete this" 的行：
   ```bash
   sed '/delete this/d' filename.txt
   ```

4. **插入行**
   在第 2 行之前插入 "New Line"：
   ```bash
   sed '2i New Line' filename.txt
   ```

5. **顯示特定行**
   只顯示第 3 行：
   ```bash
   sed -n '3p' filename.txt
   ```

## Tips
- 使用 `-i.bak` 選項可以在修改文件之前備份原始文件。
- 組合多個 `-e` 選項可以在一個命令中執行多個編輯操作。
- 測試命令時，先不使用 `-i` 選項，以避免意外修改文件。