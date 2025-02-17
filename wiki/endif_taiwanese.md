# [Linux] Bash endif 用法: 結束條件判斷

## Overview
`endif` 是一個用於 Bash 腳本中的命令，用來標示條件判斷的結束。它通常與 `if` 命令搭配使用，幫助開發者清晰地結束條件語句。

## Usage
基本語法如下：
```
endif
```

## Common Options
`endif` 本身並不接受任何選項，因為它的功能僅限於結束一個 `if` 條件語句。

## Common Examples

### 範例 1: 基本的 if-endif 結構
```bash
if [ "$VAR" -eq 1 ]; then
    echo "VAR 是 1"
endif
```

### 範例 2: 使用 else 結構
```bash
if [ "$VAR" -eq 1 ]; then
    echo "VAR 是 1"
else
    echo "VAR 不是 1"
endif
```

### 範例 3: 嵌套的 if 結構
```bash
if [ "$VAR" -gt 0 ]; then
    echo "VAR 大於 0"
    if [ "$VAR" -lt 10 ]; then
        echo "VAR 小於 10"
    endif
endif
```

## Tips
- 確保每個 `if` 都有相對應的 `endif`，以避免語法錯誤。
- 使用適當的縮排來提高可讀性，特別是在有多層嵌套的情況下。
- 在複雜的條件判斷中，考慮使用 `else` 和 `elif` 來簡化邏輯結構。