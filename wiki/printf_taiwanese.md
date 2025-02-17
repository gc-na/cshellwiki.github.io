# [Linux] Bash printf 用法: 格式化輸出文本

## Overview
`printf` 命令用於格式化輸出文本，類似於 C 語言中的 `printf` 函數。它可以將數據以特定格式輸出到標準輸出或文件中，並提供更高的靈活性和控制。

## Usage
基本語法如下：
```bash
printf [options] [arguments]
```

## Common Options
- `-v var`: 將格式化的輸出賦值給變數 `var`。
- `--help`: 顯示幫助信息。
- `--version`: 顯示版本信息。

## Common Examples
1. **基本格式化輸出**
   ```bash
   printf "Hello, %s!\n" "World"
   ```
   輸出：`Hello, World!`

2. **格式化數字**
   ```bash
   printf "Number: %.2f\n" 3.14159
   ```
   輸出：`Number: 3.14`

3. **多個參數**
   ```bash
   printf "%s is %d years old.\n" "Alice" 30
   ```
   輸出：`Alice is 30 years old.`

4. **使用變數**
   ```bash
   name="Bob"
   age=25
   printf "%s is %d years old.\n" "$name" "$age"
   ```
   輸出：`Bob is 25 years old.`

5. **輸出到文件**
   ```bash
   printf "This is a test.\n" > output.txt
   ```

## Tips
- 使用 `%.nf` 來控制浮點數的顯示位數。
- 注意格式字符串中的轉義字符，例如 `\n` 代表換行。
- 可以使用變數來提高可讀性和靈活性。