# [Linux] Bash env 使用方法: 環境變數管理

## Overview
`env` 命令用於顯示或設定環境變數。它可以用來運行指定的命令，並在執行時修改環境變數，這對於測試和執行不同環境下的程式非常有用。

## Usage
基本語法如下：
```
env [options] [arguments]
```

## Common Options
- `-i`：清空環境變數，並使用空的環境執行命令。
- `-u`：刪除指定的環境變數。
- `-0`：以 null 字元結束輸出，通常用於與其他命令的管道配合使用。

## Common Examples
1. 顯示當前環境變數：
   ```bash
   env
   ```

2. 使用新的環境變數執行命令：
   ```bash
   env VAR_NAME=value command_name
   ```

3. 清空環境變數並執行命令：
   ```bash
   env -i command_name
   ```

4. 刪除特定環境變數並執行命令：
   ```bash
   env -u VAR_NAME command_name
   ```

5. 將環境變數輸出為 null 字元結束的格式：
   ```bash
   env -0
   ```

## Tips
- 使用 `env` 來測試程式在不同環境變數下的行為，這樣可以避免對全局環境的影響。
- 結合 `-i` 選項可以幫助你確保命令在一個乾淨的環境中執行，這對於排除故障非常有用。
- 當需要在腳本中使用特定的環境變數時，考慮使用 `env` 來確保正確的變數被設置。