# [台灣] Bash mkdir 用法: 創建目錄

## Overview
`mkdir` 是一個用於在檔案系統中創建新目錄的命令。這個命令可以幫助用戶組織檔案，並在需要的時候創建新的資料夾。

## Usage
基本語法如下：
```
mkdir [選項] [參數]
```

## Common Options
- `-p`：如果父目錄不存在，則同時創建父目錄。
- `-m`：設定新目錄的權限模式。
- `-v`：顯示詳細的創建過程。

## Common Examples
1. 創建一個新目錄：
   ```bash
   mkdir new_directory
   ```

2. 同時創建多個目錄：
   ```bash
   mkdir dir1 dir2 dir3
   ```

3. 使用 `-p` 選項創建多層目錄：
   ```bash
   mkdir -p parent_directory/child_directory
   ```

4. 設定目錄權限：
   ```bash
   mkdir -m 755 new_directory
   ```

5. 顯示創建過程：
   ```bash
   mkdir -v new_directory
   ```

## Tips
- 使用 `-p` 選項可以避免因為父目錄不存在而導致的錯誤。
- 在創建目錄時，考慮使用有意義的名稱，以便於未來的檔案管理。
- 定期檢查和整理目錄結構，保持系統整潔。