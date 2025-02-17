# [Linux] Bash continue 用法: 繼續執行迴圈

## Overview
`continue` 命令用於在迴圈中跳過當前的迭代，並直接進入下一次迭代。這在需要根據特定條件跳過某些步驟時非常有用。

## Usage
基本語法如下：
```bash
continue [n]
```
這裡的 `n` 是可選的，表示跳過的迭代次數。

## Common Options
- `n`: 指定要跳過的迭代次數。如果不指定，則默認為 1，表示跳過當前迭代。

## Common Examples
1. **基本用法**：在 `for` 迴圈中跳過特定的數字。
   ```bash
   for i in {1..5}; do
       if [ $i -eq 3 ]; then
           continue
       fi
       echo $i
   done
   ```
   這段程式碼將輸出 1, 2, 4, 5，跳過了 3。

2. **在 `while` 迴圈中使用**：
   ```bash
   count=0
   while [ $count -lt 5 ]; do
       count=$((count + 1))
       if [ $count -eq 2 ]; then
           continue
       fi
       echo $count
   done
   ```
   這段程式碼將輸出 1, 3, 4, 5，跳過了 2。

3. **使用 `n` 參數跳過多次迭代**：
   ```bash
   for i in {1..10}; do
       if [ $i -lt 5 ]; then
           continue 2
       fi
       echo $i
   done
   ```
   這段程式碼將輸出 5, 6, 7, 8, 9, 10，跳過了 1 到 4。

## Tips
- 使用 `continue` 時，確保條件判斷正確，以避免無意中跳過重要的迭代。
- 在複雜的迴圈中，考慮使用註解來提高可讀性，讓其他人更容易理解你的邏輯。
- 測試你的迴圈邏輯，確保 `continue` 的使用不會導致無窮迴圈或錯誤的結果。