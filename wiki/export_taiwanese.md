# [Linux] Bash export 使用法: 環境變數的設定與導出

## Overview
`export` 命令用於設定或導出環境變數，使得這些變數可以被當前 shell 及其子進程所使用。這對於在 shell 腳本或命令行中傳遞參數非常有用。

## Usage
基本語法如下：
```bash
export [options] [arguments]
```

## Common Options
- `-p`：顯示所有已導出的環境變數。
- `-n`：取消導出指定的變數，使其不再是環境變數。
- `-f`：導出函數，而不僅僅是變數。

## Common Examples
1. 導出一個變數：
   ```bash
   MY_VAR="Hello, World!"
   export MY_VAR
   ```

2. 同時導出多個變數：
   ```bash
   export VAR1="Value1" VAR2="Value2"
   ```

3. 顯示所有導出的變數：
   ```bash
   export -p
   ```

4. 取消導出一個變數：
   ```bash
   export -n MY_VAR
   ```

5. 導出一個函數：
   ```bash
   my_function() {
       echo "This is a function."
   }
   export -f my_function
   ```

## Tips
- 確保在導出變數之前已經為其賦值，否則導出的變數將是空的。
- 使用 `export -p` 可以檢查當前所有導出的環境變數，這對於調試非常有幫助。
- 導出變數後，這些變數將在子進程中可用，因此可以在執行其他腳本或命令時使用。