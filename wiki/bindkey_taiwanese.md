# [Linux] Bash bindkey 使用方法: 設定鍵盤快捷鍵

## Overview
`bindkey` 是一個用於設定和管理鍵盤快捷鍵的命令，主要在 Zsh 環境中使用。透過這個命令，使用者可以自訂鍵盤按鍵的功能，以提高操作效率。

## Usage
基本語法如下：
```bash
bindkey [options] [arguments]
```

## Common Options
- `-L`：列出所有當前的鍵盤綁定。
- `-e`：使用 Emacs 鍵綁定風格。
- `-v`：使用 Vi 鍵綁定風格。
- `-s`：將按鍵序列綁定到指定的命令。

## Common Examples
以下是一些常見的 `bindkey` 使用範例：

1. 列出當前的鍵盤綁定：
   ```bash
   bindkey -L
   ```

2. 將 `Ctrl+X` 綁定為 `exit` 命令：
   ```bash
   bindkey '^X' exit
   ```

3. 使用 Emacs 鍵綁定風格：
   ```bash
   bindkey -e
   ```

4. 將 `F2` 鍵綁定為顯示當前日期：
   ```bash
   bindkey -s 'F2' 'date\n'
   ```

## Tips
- 在修改鍵盤綁定之前，建議先備份當前的設定，以便隨時恢復。
- 使用 `bindkey -L` 來檢查現有的綁定，避免衝突。
- 可以將常用的綁定添加到你的 `.zshrc` 檔案中，以便每次啟動終端時自動加載。