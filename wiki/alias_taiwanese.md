# [Linux] Bash alias 用法: 簡化命令

## Overview
`alias` 命令用來為其他命令創建簡短的別名，這樣可以讓使用者更方便地執行常用的命令。透過使用別名，使用者可以減少輸入的字元，並提高工作效率。

## Usage
基本語法如下：
```
alias [options] [arguments]
```

## Common Options
- `-p`：顯示所有當前的別名。
- `--help`：顯示幫助信息。

## Common Examples
以下是一些常用的 `alias` 示例：

1. 為 `ls -la` 創建別名：
   ```bash
   alias ll='ls -la'
   ```

2. 為 `git status` 創建別名：
   ```bash
   alias gs='git status'
   ```

3. 為 `rm -i` 創建別名，增加刪除文件的安全性：
   ```bash
   alias rm='rm -i'
   ```

4. 為 `clear` 創建別名，簡化清屏命令：
   ```bash
   alias c='clear'
   ```

## Tips
- 使用 `alias` 時，建議在你的 `~/.bashrc` 或 `~/.bash_profile` 文件中添加別名，以便在每次啟動終端時自動加載。
- 選擇簡短且易於記憶的別名，這樣可以提高工作效率。
- 定期檢查和清理不再使用的別名，以保持環境的整潔。