# [Linux] Bash if 條件判斷: 用於執行條件式的命令

## Overview
`if` 命令用於根據條件判斷執行不同的命令。它是 Bash 腳本中常用的控制結構，能夠根據條件的真假來決定執行的路徑。

## Usage
基本語法如下：
```bash
if [條件 ]; then
    # 執行的命令
fi
```

## Common Options
- `-e`: 檢查檔案是否存在。
- `-d`: 檢查檔案是否為目錄。
- `-f`: 檢查檔案是否為常規檔案。
- `-z`: 檢查字串是否為空。
- `-n`: 檢查字串是否不為空。

## Common Examples

### 檢查檔案是否存在
```bash
if [ -e "example.txt" ]; then
    echo "檔案存在"
else
    echo "檔案不存在"
fi
```

### 檢查字串是否為空
```bash
name=""
if [ -z "$name" ]; then
    echo "名字是空的"
else
    echo "名字是: $name"
fi
```

### 檢查目錄是否存在
```bash
if [ -d "/home/user" ]; then
    echo "目錄存在"
else
    echo "目錄不存在"
fi
```

### 使用邏輯運算符
```bash
value=10
if [ $value -gt 5 ] && [ $value -lt 15 ]; then
    echo "值在範圍內"
else
    echo "值不在範圍內"
fi
```

## Tips
- 確保在條件判斷中使用正確的空格，因為 Bash 對空格非常敏感。
- 使用 `elif` 可以增加多個條件判斷，讓程式碼更具彈性。
- 在條件中使用雙中括號 `[[ ]]` 可以提供更強大的條件判斷功能，例如正則表達式匹配。