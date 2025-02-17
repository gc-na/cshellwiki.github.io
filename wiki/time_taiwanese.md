# [台灣] Bash time 使用法: 測量執行時間

## Overview
`time` 命令用於測量執行一個命令所需的時間。它會顯示該命令的實際執行時間、用於用戶模式的 CPU 時間以及系統模式的 CPU 時間，這對於性能分析非常有用。

## Usage
基本語法如下：
```
time [options] [arguments]
```

## Common Options
- `-p`：以 POSIX 標準格式顯示輸出。
- `-o FILE`：將輸出寫入指定的文件。
- `-a`：將輸出附加到指定的文件中，而不是覆蓋。

## Common Examples
以下是一些常見的使用範例：

1. 測量一個簡單命令的執行時間：
   ```bash
   time ls -l
   ```

2. 將輸出寫入文件：
   ```bash
   time -o output.txt sleep 2
   ```

3. 使用 POSIX 格式顯示時間：
   ```bash
   time -p sleep 3
   ```

4. 附加輸出到文件：
   ```bash
   time -a -o output.txt sleep 4
   ```

## Tips
- 在測試性能時，確保環境一致，以獲得準確的測量結果。
- 對於長時間運行的命令，考慮使用 `-o` 選項來保存結果，方便後續分析。
- 使用 `time` 命令時，注意它的輸出會顯示在標準錯誤流中，而不是標準輸出流。