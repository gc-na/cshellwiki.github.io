# [Linux] Bash yes 用法: 自動重複輸出

## Overview
`yes` 命令是一個簡單的工具，用來不斷輸出指定的字符串，通常是 "y" 或 "yes"。這個命令在需要自動確認的情況下非常有用，例如在安裝過程中自動回答提示。

## Usage
基本語法如下：
```
yes [options] [arguments]
```

## Common Options
- `-n`：不輸出換行符。
- `--help`：顯示幫助信息。
- `--version`：顯示版本信息。

## Common Examples
以下是一些常見的使用範例：

1. **輸出 "y"**：
   ```bash
   yes y
   ```

2. **自動確認安裝**：
   ```bash
   yes | sudo apt-get install package-name
   ```

3. **輸出自定義字符串**：
   ```bash
   yes "I agree" | head -n 5
   ```

4. **不斷輸出 "no"**：
   ```bash
   yes no
   ```

## Tips
- 使用 `yes` 時，請注意它會無限輸出，建議搭配其他命令使用，以避免終端機被填滿。
- 可以使用 `head` 或 `tail` 限制輸出的行數，例如 `yes | head -n 10` 只輸出前十行。
- 在需要自動化腳本中確認提示時，`yes` 是一個非常方便的工具。