# [Linux] Bash else 使用法: 用於條件判斷的命令

## Overview
`else` 是 Bash 中的一個條件語句，用於在 `if` 條件不成立時執行替代的指令。它通常與 `if` 語句一起使用，幫助用戶根據不同的條件執行不同的操作。

## Usage
基本語法如下：
```bash
if [ condition ]; then
    # 當條件成立時執行的指令
else
    # 當條件不成立時執行的指令
fi
```

## Common Options
`else` 本身沒有選項，但它通常與 `if` 語句一起使用。以下是 `if` 語句的一些常見選項：
- `-e`：檢查檔案是否存在。
- `-f`：檢查檔案是否為常規檔案。
- `-d`：檢查檔案是否為目錄。

## Common Examples
以下是一些使用 `else` 的實際範例：

### 範例 1：檢查檔案是否存在
```bash
if [ -e myfile.txt ]; then
    echo "檔案存在"
else
    echo "檔案不存在"
fi
```

### 範例 2：檢查目錄是否存在
```bash
if [ -d mydirectory ]; then
    echo "目錄存在"
else
    echo "目錄不存在"
fi
```

### 範例 3：檢查變數是否為空
```bash
if [ -z "$myvar" ]; then
    echo "變數是空的"
else
    echo "變數有值"
fi
```

## Tips
- 確保在 `if` 和 `else` 之間使用 `then` 和 `fi`，以正確結束條件語句。
- 使用適當的條件檢查來避免不必要的錯誤。
- 可以在 `else` 中嵌套其他 `if` 語句，以處理更複雜的邏輯。