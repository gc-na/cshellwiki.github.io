# [Linux] Bash echo 用法: 輸出文字到終端

## Overview
`echo` 命令用於在終端顯示文字或變數的值。它是一個非常基本但重要的命令，常用於腳本中來顯示訊息或輸出結果。

## Usage
基本語法如下：
```
echo [options] [arguments]
```

## Common Options
- `-n`: 不在輸出結尾添加換行符。
- `-e`: 啟用轉義字符，例如 `\n`（換行）和 `\t`（製表符）。
- `-E`: 禁用轉義字符（這是預設行為）。

## Common Examples
1. **輸出簡單文字**
   ```bash
   echo "Hello, World!"
   ```

2. **不換行輸出**
   ```bash
   echo -n "This is on the same line."
   ```

3. **使用轉義字符**
   ```bash
   echo -e "Line 1\nLine 2"
   ```

4. **顯示變數的值**
   ```bash
   name="Alice"
   echo "My name is $name."
   ```

5. **輸出帶有製表符的文字**
   ```bash
   echo -e "Column1\tColumn2"
   ```

## Tips
- 使用 `-n` 選項可以讓你在輸出後不換行，這在需要連續輸出時非常有用。
- 當需要格式化輸出時，使用 `-e` 選項可以讓你更靈活地控制輸出格式。
- 在腳本中使用 `echo` 時，確保變數已正確設置，以避免顯示空值。