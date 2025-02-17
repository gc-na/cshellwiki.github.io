# [Linux] Bash mv 使用法: 移動或重命名檔案

## Overview
`mv` 命令用於移動或重命名檔案和目錄。這是一個非常實用的命令，能夠幫助用戶有效地管理檔案系統中的資料。

## Usage
基本語法如下：
```
mv [選項] [來源] [目標]
```

## Common Options
- `-i`：在覆蓋檔案之前提示用戶確認。
- `-u`：僅在來源檔案比目標檔案新時才進行移動。
- `-v`：顯示詳細的操作過程，讓用戶知道正在進行的動作。

## Common Examples
1. **移動檔案**
   ```bash
   mv file.txt /path/to/destination/
   ```

2. **重命名檔案**
   ```bash
   mv oldname.txt newname.txt
   ```

3. **使用 -i 選項進行安全移動**
   ```bash
   mv -i file.txt /path/to/destination/
   ```

4. **使用 -u 選項僅移動更新的檔案**
   ```bash
   mv -u file.txt /path/to/destination/
   ```

5. **顯示詳細過程**
   ```bash
   mv -v file.txt /path/to/destination/
   ```

## Tips
- 在使用 `mv` 命令時，建議先使用 `-i` 選項，以避免意外覆蓋重要檔案。
- 使用 `-v` 選項可以幫助你追蹤檔案的移動過程，特別是在處理大量檔案時。
- 確保目標路徑存在，否則 `mv` 會將檔案重命名為目標名稱，而不是移動到目標目錄。