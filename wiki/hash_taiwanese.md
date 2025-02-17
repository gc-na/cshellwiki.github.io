# [Linux] Bash hash 使用法: 查詢和管理命令的哈希值

## Overview
`hash` 命令用於管理和查詢命令的哈希值。當你在 Bash 中執行命令時，系統會記錄這些命令的路徑，以加快未來的執行速度。使用 `hash` 命令可以查看這些哈希值，或清除特定的哈希記錄。

## Usage
基本語法如下：
```
hash [options] [arguments]
```

## Common Options
- `-r`：重置哈希表，清除所有已記錄的命令。
- `-p`：指定一個命令的完整路徑，並將其添加到哈希表中。
- `-l`：列出當前哈希表中的所有命令及其對應的路徑。

## Common Examples
以下是一些常見的使用範例：

1. **查看當前哈希表**
   ```bash
   hash
   ```

2. **重置哈希表**
   ```bash
   hash -r
   ```

3. **添加特定命令到哈希表**
   ```bash
   hash -p /usr/local/bin/mycommand mycommand
   ```

4. **列出哈希表中的所有命令**
   ```bash
   hash -l
   ```

## Tips
- 定期使用 `hash -r` 來清理過時的命令記錄，特別是在安裝或卸載軟體後。
- 使用 `hash` 命令可以幫助你快速確認某個命令的路徑，避免使用 `which` 或 `whereis`。
- 如果你在使用某個命令時遇到問題，檢查哈希表可能會發現路徑已經改變。