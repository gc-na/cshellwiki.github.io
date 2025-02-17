# [Linux] Bash source 使用法: 讀取和執行檔案中的命令

## Overview
`source` 命令用於在當前的 shell 環境中讀取和執行指定檔案中的命令。這意味著它可以用來載入環境變數或函數，而不需要啟動新的 shell 實例。

## Usage
基本語法如下：
```bash
source [options] [arguments]
```

## Common Options
- `-h`, `--help`: 顯示幫助信息。
- `-V`, `--version`: 顯示版本信息。

## Common Examples
以下是一些常見的使用範例：

1. 讀取並執行一個名為 `script.sh` 的檔案：
   ```bash
   source script.sh
   ```

2. 使用 `.` 符號來達到相同效果：
   ```bash
   . script.sh
   ```

3. 讀取一個包含環境變數的檔案，例如 `env.sh`：
   ```bash
   source env.sh
   ```

4. 在 `.bashrc` 中載入修改後的環境變數：
   ```bash
   source ~/.bashrc
   ```

## Tips
- 確保檔案具有執行權限，否則可能會遇到權限錯誤。
- 使用 `source` 可以避免創建新的 shell 實例，這對於環境變數的即時更新特別有用。
- 在編輯 `.bashrc` 或 `.bash_profile` 後，記得使用 `source` 來立即應用變更。