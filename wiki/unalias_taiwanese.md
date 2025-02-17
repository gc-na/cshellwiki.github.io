# [台灣] Bash unalias 使用方法: 解除別名

## Overview
`unalias` 命令用於刪除已定義的別名，這樣在命令行中輸入的命令將不再被替換為其別名。

## Usage
基本語法如下：
```
unalias [options] [arguments]
```

## Common Options
- `-a`：刪除所有別名。
- `-p`：顯示當前所有的別名。

## Common Examples
1. 刪除單個別名：
   ```bash
   unalias ll
   ```

2. 刪除所有別名：
   ```bash
   unalias -a
   ```

3. 顯示當前所有別名：
   ```bash
   unalias -p
   ```

## Tips
- 在使用 `unalias` 前，可以使用 `alias` 命令檢查目前的別名設定。
- 如果你想在每次啟動 shell 時自動刪除某些別名，可以將 `unalias` 命令添加到你的 shell 配置檔（如 `.bashrc` 或 `.bash_profile`）中。