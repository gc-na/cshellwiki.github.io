# [Linux] Bash csplit 用法: 分割檔案

## Overview
`csplit` 是一個用於將檔案根據指定的模式或行數進行分割的命令。這個工具非常適合處理大型文本檔案，讓使用者可以根據需求將檔案拆分成多個小檔案。

## Usage
基本語法如下：
```bash
csplit [選項] [參數]
```

## Common Options
- `-f PREFIX`：指定生成檔案的前綴名。
- `-n NUM`：指定生成檔案的數字位數。
- `-b SUFFIX`：指定生成檔案的後綴名。
- `-k`：保留未使用的檔案，即使在出錯時也不刪除。

## Common Examples
以下是一些常見的使用範例：

1. **根據行數分割檔案**：
   將 `file.txt` 每 10 行分割一次。
   ```bash
   csplit file.txt 10
   ```

2. **使用模式分割檔案**：
   根據包含 "START" 的行分割 `file.txt`。
   ```bash
   csplit file.txt /START/
   ```

3. **指定檔案前綴**：
   將 `file.txt` 分割，每 5 行生成的檔案前綴為 `part_`。
   ```bash
   csplit -f part_ file.txt 5
   ```

4. **指定檔案數字位數**：
   將 `file.txt` 每 3 行分割，並將檔案命名為 `file00`, `file01` 等。
   ```bash
   csplit -n 2 file.txt 3
   ```

## Tips
- 在使用 `csplit` 時，建議先備份原始檔案，以防不小心刪除或損壞。
- 使用 `-k` 選項可以在出錯時保留所有生成的檔案，方便進行後續檢查。
- 可以結合其他命令如 `grep` 來先過濾檔案內容，再進行分割，這樣可以提高效率。