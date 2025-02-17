# [台灣] Bash nohup 使用法: 允許程序在登出後繼續執行

## Overview
`nohup` 是一個用於在登出或關閉終端後，讓程序繼續運行的命令。這對於需要長時間執行的任務特別有用，因為它可以防止程序因為終端關閉而被終止。

## Usage
基本語法如下：
```bash
nohup [選項] [命令] [參數] &
```

## Common Options
- `&`：將命令放在背景執行。
- `-h`：顯示幫助信息。
- `-p`：指定進程ID。

## Common Examples
1. 在背景中運行一個長時間執行的腳本：
   ```bash
   nohup ./long_running_script.sh &
   ```

2. 將輸出重定向到一個文件：
   ```bash
   nohup ./my_program > output.log &
   ```

3. 同時將標準錯誤輸出重定向到文件：
   ```bash
   nohup ./my_program > output.log 2>&1 &
   ```

4. 使用 `nohup` 執行 Python 腳本：
   ```bash
   nohup python3 my_script.py &
   ```

## Tips
- 確保在使用 `nohup` 時，將輸出重定向到文件，這樣可以方便查看程序的執行結果。
- 使用 `jobs` 命令來查看當前背景執行的任務。
- 如果需要停止背景進程，可以使用 `kill` 命令加上進程ID。