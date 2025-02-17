# [台灣] Bash stty 使用說明：控制終端機的行為

## Overview
`stty` 是一個用於設定和顯示終端機行為的命令。它可以用來調整輸入和輸出的特性，例如改變行為、設定特殊鍵的功能等。

## Usage
基本語法如下：
```
stty [options] [arguments]
```

## Common Options
- `-a`：顯示所有當前的設定。
- `-g`：顯示當前的設定為一個可儲存的格式。
- `erase`：設定刪除鍵的功能。
- `kill`：設定行為鍵的功能，用於刪除整行。
- `intr`：設定中斷鍵的功能。

## Common Examples
以下是一些常見的 `stty` 使用範例：

1. 顯示當前的終端機設定：
   ```bash
   stty -a
   ```

2. 設定刪除鍵為 Backspace：
   ```bash
   stty erase ^H
   ```

3. 設定中斷鍵為 Ctrl+C：
   ```bash
   stty intr ^C
   ```

4. 將行為鍵設定為 Ctrl+U：
   ```bash
   stty kill ^U
   ```

5. 將當前設定儲存為變數：
   ```bash
   saved_stty=$(stty -g)
   ```

## Tips
- 在更改設定之前，建議先使用 `stty -g` 儲存當前設定，以便隨時恢復。
- 使用 `stty -a` 來檢查所有設定，這有助於了解目前的終端機狀態。
- 在腳本中使用 `stty` 時，注意在執行後恢復原始設定，以免影響後續操作。