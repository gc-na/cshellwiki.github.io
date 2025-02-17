# [Linux] Bash true 使用法: 總是返回成功的命令

## Overview
`true` 是一個非常簡單的命令，它的主要功能是返回成功的退出狀態碼（0）。這在需要一個始終成功的命令時非常有用，特別是在腳本中。

## Usage
基本語法如下：
```
true [options] [arguments]
```

## Common Options
`true` 命令本身不接受任何選項或參數，因為它的唯一目的是返回成功的狀態碼。

## Common Examples
以下是一些 `true` 命令的實用範例：

1. **在條件語句中使用**
   ```bash
   if true; then
       echo "這個條件永遠成立"
   fi
   ```

2. **用於循環中**
   ```bash
   while true; do
       echo "這個循環會一直執行"
       sleep 1
   done
   ```

3. **在腳本中作為佔位符**
   ```bash
   #!/bin/bash
   true # 這裡可以替換為其他命令
   echo "這個腳本會繼續執行"
   ```

## Tips
- `true` 可以用來測試其他命令的結構，特別是在開發和測試階段。
- 在需要一個不執行任何操作的命令時，可以使用 `true` 作為佔位符，以保持腳本的完整性。