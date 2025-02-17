# [Linux] Bash case 用法: 根據模式執行條件

## Overview
`case` 命令是一個用於模式匹配的條件語句，允許根據變數的值執行不同的命令。這在需要根據不同情況執行特定操作時非常有用。

## Usage
基本語法如下：
```bash
case [變數] in
    [模式1])
        [命令1]
        ;;
    [模式2])
        [命令2]
        ;;
    *)
        [預設命令]
        ;;
esac
```

## Common Options
`case` 命令本身沒有特別的選項，但可以與其他命令結合使用以增強功能。

## Common Examples

### 範例 1: 簡單的模式匹配
```bash
read -p "請輸入顏色: " color
case $color in
    "紅色")
        echo "你選擇了紅色"
        ;;
    "藍色")
        echo "你選擇了藍色"
        ;;
    *)
        echo "未知顏色"
        ;;
esac
```

### 範例 2: 檔案擴展名處理
```bash
filename="example.txt"
case $filename in
    *.txt)
        echo "這是一個文本檔案"
        ;;
    *.jpg|*.png)
        echo "這是一個圖片檔案"
        ;;
    *)
        echo "未知檔案類型"
        ;;
esac
```

### 範例 3: 數字範圍匹配
```bash
read -p "請輸入一個數字: " num
case $num in
    [1-9])
        echo "你輸入的是一位數字"
        ;;
    [1-9][0-9])
        echo "你輸入的是兩位數字"
        ;;
    *)
        echo "輸入不在範圍內"
        ;;
esac
```

## Tips
- 使用 `*)` 來處理所有未匹配的情況，這樣可以避免錯誤。
- 確保每個模式後面都有 `;;`，以正確結束該條件。
- `case` 命令對於處理多個條件非常有效，特別是在選擇或選項的情況下。