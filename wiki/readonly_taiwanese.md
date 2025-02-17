# [Linux] Bash readonly 用法: 設定變數為唯讀

## Overview
`readonly` 命令用來將變數設定為唯讀，這意味著一旦變數被設定為唯讀，就無法再被修改或刪除。這在腳本中非常有用，可以防止意外改變重要的變數。

## Usage
基本語法如下：
```bash
readonly [options] [arguments]
```

## Common Options
- `-p`: 列出所有唯讀變數及其值。

## Common Examples
以下是一些常見的使用範例：

### 設定變數為唯讀
```bash
my_var="Hello, World!"
readonly my_var
```

### 嘗試修改唯讀變數（會失敗）
```bash
my_var="New Value"  # 這行會報錯
```

### 列出所有唯讀變數
```bash
readonly -p
```

### 使用唯讀變數
```bash
readonly my_path="/usr/local/bin"
echo $my_path  # 輸出: /usr/local/bin
```

## Tips
- 在腳本中使用 `readonly` 可以幫助維護變數的穩定性，避免意外的修改。
- 將重要的設定變數設為唯讀，以確保它們不會在程式執行過程中被改變。