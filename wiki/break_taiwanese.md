# [Linux] Bash break 用法: 結束迴圈

## Overview
`break` 命令用於結束一個迴圈的執行，無論是 `for`、`while` 還是 `until` 迴圈。當 `break` 被執行時，控制權會跳出當前的迴圈，繼續執行迴圈後的程式碼。

## Usage
基本語法如下：
```bash
break [n]
```
其中 `n` 是可選的，表示要跳出幾層迴圈，預設為 1。

## Common Options
- `n`: 指定要跳出幾層迴圈。若不指定，則只跳出最近的一層迴圈。

## Common Examples

### 結束最近的迴圈
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        break
    fi
    echo $i
done
```
這段程式碼會輸出 1 和 2，當 `i` 等於 3 時，迴圈會被 `break` 結束。

### 跳出多層迴圈
```bash
outer_loop: for i in {1..3}; do
    for j in {1..3}; do
        if [ $i -eq 2 ] && [ $j -eq 2 ]; then
            break outer_loop
        fi
        echo "$i $j"
    done
done
```
這段程式碼會在 `i` 和 `j` 都等於 2 時，跳出外層迴圈，輸出結果為：
```
1 1
1 2
1 3
2 1
2 2
```

## Tips
- 使用標籤（label）來跳出多層迴圈時，確保標籤名稱是唯一的，這樣可以避免混淆。
- 在使用 `break` 時，注意迴圈的邏輯，確保在適當的條件下才會結束迴圈，避免無限迴圈的情況發生。