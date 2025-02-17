# [台灣] Bash tmux 使用法: 多工管理工具

## Overview
tmux 是一個終端多工管理器，允許用戶在單一的終端窗口中運行多個會話。這使得用戶可以在不同的會話之間輕鬆切換，並且能夠在斷線後重新連接到先前的會話。

## Usage
tmux 的基本語法如下：

```bash
tmux [options] [arguments]
```

## Common Options
- `new`：創建一個新的 tmux 會話。
- `attach`：連接到已存在的 tmux 會話。
- `detach`：從當前會話中分離。
- `list-sessions`：列出所有當前的 tmux 會話。
- `kill-session`：終止指定的 tmux 會話。

## Common Examples
以下是一些常見的 tmux 使用範例：

1. 創建一個新的 tmux 會話：
   ```bash
   tmux new -s mysession
   ```

2. 連接到一個已存在的會話：
   ```bash
   tmux attach -t mysession
   ```

3. 分離當前的會話：
   ```bash
   Ctrl+b d
   ```

4. 列出所有會話：
   ```bash
   tmux list-sessions
   ```

5. 終止一個會話：
   ```bash
   tmux kill-session -t mysession
   ```

## Tips
- 使用 `Ctrl+b` 作為 tmux 的前綴鍵，這樣可以方便地執行其他命令。
- 可以使用 `split-window` 命令將窗口分割為上下或左右兩個部分，方便同時查看多個終端。
- 定期使用 `detach` 功能，這樣可以在需要時快速回到會話而不會丟失進度。