# [Linux] Bash users 使用者: 列出系統中的使用者

## Overview
`users` 命令用於顯示當前登入系統的所有使用者名稱。這個命令非常簡單，通常用於快速查看哪些使用者正在使用系統。

## Usage
基本語法如下：
```
users [options] [arguments]
```

## Common Options
- `-n`：顯示使用者的數量。
- `-r`：顯示登入的使用者的完整名稱。

## Common Examples
以下是一些常見的使用範例：

1. 顯示當前登入的所有使用者：
   ```bash
   users
   ```

2. 顯示當前登入的使用者數量：
   ```bash
   users -n
   ```

3. 顯示登入使用者的完整名稱：
   ```bash
   users -r
   ```

## Tips
- `users` 命令的輸出不會顯示重複的使用者名稱，因此如果同一使用者多次登入，只會顯示一次。
- 可以將 `users` 命令與其他命令結合使用，例如 `wc -w` 來計算當前登入的使用者數量：
  ```bash
  users | wc -w
  ```
- 在多使用者環境中，定期檢查登入的使用者可以幫助管理系統安全性。