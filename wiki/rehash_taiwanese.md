# [台灣] Bash rehash 用法: 重新整理命令快取

## Overview
`rehash` 命令用於更新 Bash 的命令快取，這樣當你新增或刪除可執行文件時，Bash 可以正確識別這些變更。

## Usage
基本語法如下：
```bash
rehash [options] [arguments]
```

## Common Options
- `-p`：僅更新 PATH 中的命令快取，不會更新其他路徑的快取。

## Common Examples
以下是一些常見的使用範例：

1. **基本使用**：
   ```bash
   rehash
   ```
   這會更新所有的命令快取。

2. **使用 -p 選項**：
   ```bash
   rehash -p
   ```
   僅更新 PATH 中的命令快取。

3. **在安裝新軟體後使用**：
   ```bash
   sudo apt install new-software
   rehash
   ```
   安裝新軟體後，使用 `rehash` 來確保 Bash 知道新命令。

## Tips
- 在安裝或刪除可執行文件後，記得執行 `rehash` 以避免命令找不到的問題。
- 使用 `rehash -p` 可以更快地更新命令快取，特別是在 PATH 中有大量命令時。
- 如果你使用的是 Zsh，`rehash` 也可以用來更新命令快取，功能類似。