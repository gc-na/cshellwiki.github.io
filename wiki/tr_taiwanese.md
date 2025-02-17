# [Linux] Bash tr 用法: 轉換或刪除字符

## Overview
`tr` 是一個用於轉換或刪除輸入文本中字符的命令。它可以用來替換字符、刪除字符或壓縮重複的字符，通常用於文本處理和數據清理。

## Usage
基本語法如下：
```bash
tr [options] [arguments]
```

## Common Options
- `-d`：刪除指定的字符。
- `-s`：壓縮重複的字符為單一字符。
- `-c`：指定要轉換的字符集的補集。

## Common Examples

### 1. 替換字符
將文本中的小寫字母轉換為大寫字母：
```bash
echo "hello world" | tr 'a-z' 'A-Z'
```

### 2. 刪除字符
刪除文本中的所有數字：
```bash
echo "abc123def456" | tr -d '0-9'
```

### 3. 壓縮重複字符
將連續的空格壓縮為單一空格：
```bash
echo "This    is    a    test." | tr -s ' '
```

### 4. 使用補集
將所有非字母字符替換為下劃線：
```bash
echo "Hello, World! 123" | tr -c 'a-zA-Z' '_'
```

## Tips
- 使用 `echo` 和管道 (`|`) 結合 `tr` 可以方便地處理輸入文本。
- 注意字符集的順序，因為 `tr` 是逐字符替換的。
- 可以將 `tr` 與其他命令結合使用，例如 `grep` 或 `sed`，以增強文本處理能力。