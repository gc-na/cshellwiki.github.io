# [Linux] Bash while 使用法: 用於重複執行命令

## Overview
`while` 命令是一個控制結構，用於在條件為真時重複執行一段命令。這使得在滿足特定條件時，可以持續執行某些操作，直到條件不再成立。

## Usage
基本語法如下：
```bash
while [條件]
do
    # 執行的命令
done
```

## Common Options
`while` 命令本身沒有特定的選項，但可以與其他命令和條件結構結合使用，例如：
- `test` 或 `[ ]`：用於評估條件。
- `break`：用於提前退出循環。
- `continue`：用於跳過當前迭代，進入下一次循環。

## Common Examples

### 基本範例
持續輸出數字，直到達到 5：
```bash
count=1
while [ $count -le 5 ]
do
    echo "Count is: $count"
    count=$((count + 1))
done
```

### 讀取文件行
逐行讀取文件並輸出：
```bash
while IFS= read -r line
do
    echo "$line"
done < filename.txt
```

### 等待用戶輸入
持續要求用戶輸入，直到輸入 "exit"：
```bash
input=""
while [ "$input" != "exit" ]
do
    read -p "Enter something (type 'exit' to quit): " input
    echo "You entered: $input"
done
```

## Tips
- 確保在循環內部有條件改變的邏輯，避免無限循環。
- 使用 `break` 和 `continue` 可以更靈活地控制循環的執行。
- 在處理文件時，使用 `IFS` 來正確讀取行，避免空格問題。