# [Linux] Bash foreach 使用法: 用於迭代執行命令

## Overview
`foreach` 是一個用於在 Bash 環境中迭代執行命令的指令。它可以讓使用者對一組項目進行循環操作，通常用於批量處理或自動化任務。

## Usage
基本語法如下：
```
foreach [options] [arguments]
```

## Common Options
- `-n`：不顯示命令的執行過程。
- `-p`：在執行每個命令前提示用戶確認。
- `-v`：顯示每個命令的詳細信息。

## Common Examples
以下是一些實用的範例：

1. **基本迴圈**
   ```bash
   foreach item in (1 2 3 4 5)
   echo $item
   end
   ```
   這段程式碼將會輸出數字 1 到 5。

2. **處理檔案**
   ```bash
   foreach file in *.txt
   cat $file
   end
   ```
   這將會顯示當前目錄下所有 `.txt` 檔案的內容。

3. **批量重命名檔案**
   ```bash
   foreach file in *.jpg
   mv $file ${file/.jpg/.png}
   end
   ```
   這段程式碼會將所有 `.jpg` 檔案轉換為 `.png` 檔案。

## Tips
- 使用 `-n` 選項可以避免在執行過程中顯示不必要的命令，讓輸出更乾淨。
- 在處理大量檔案時，建議先使用 `echo` 測試命令，確保它們正確無誤。
- 對於需要確認的操作，可以使用 `-p` 選項，以避免意外刪除或修改檔案。