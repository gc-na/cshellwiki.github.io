# [Linux] Bash clear 使用法: 清除終端機畫面

## Overview
`clear` 命令用來清除終端機的顯示內容，讓使用者的畫面變得乾淨整潔。這對於長時間使用終端機時，能夠提高可讀性和操作效率。

## Usage
基本語法如下：
```bash
clear [options] [arguments]
```

## Common Options
- `-x`：清除顯示並且不會保存任何內容到 scrollback buffer。
- `-V`：顯示版本資訊。

## Common Examples
以下是一些常見的使用範例：

1. **清除終端機畫面**：
   ```bash
   clear
   ```

2. **清除並不保留 scrollback buffer**：
   ```bash
   clear -x
   ```

3. **查看版本資訊**：
   ```bash
   clear -V
   ```

## Tips
- 使用 `clear` 可以讓你在執行長指令或查看大量輸出後，快速清理視窗。
- 若想要在腳本中自動清除畫面，可以在腳本的開頭加上 `clear` 命令。
- 在某些終端機中，按下 `Ctrl + L` 也可以達到清除畫面的效果。