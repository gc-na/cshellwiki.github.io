# [台灣] Bash tput 用法: 控制終端顯示屬性

## Overview
`tput` 是一個用於控制終端顯示屬性的命令。它可以用來設定顏色、字型樣式和其他顯示屬性，讓使用者能夠改善終端的可讀性和美觀性。

## Usage
基本語法如下：
```
tput [options] [arguments]
```

## Common Options
- `setaf [n]`：設定前景顏色，`n` 是顏色的編號。
- `setab [n]`：設定背景顏色，`n` 是顏色的編號。
- `bold`：設定文字為粗體。
- `smso`：啟用反白顯示。
- `rmso`：關閉反白顯示。
- `clear`：清除終端畫面。

## Common Examples
- 設定前景顏色為紅色：
  ```bash
  tput setaf 1
  echo "這是紅色的文字"
  ```

- 設定背景顏色為藍色：
  ```bash
  tput setab 4
  echo "這是藍色背景的文字"
  ```

- 設定文字為粗體：
  ```bash
  tput bold
  echo "這是粗體文字"
  ```

- 清除終端畫面：
  ```bash
  tput clear
  ```

- 啟用和關閉反白顯示：
  ```bash
  tput smso
  echo "這是反白顯示的文字"
  tput rmso
  ```

## Tips
- 在使用 `tput` 設定顏色時，可以參考顏色編號，通常 0-7 代表基本顏色。
- 將 `tput` 命令放入腳本中，可以自動化終端的顯示效果。
- 使用 `tput reset` 可以恢復終端的預設顯示屬性，這對於清理顯示非常有用。