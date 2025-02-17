# [Linux] Bash killall 用法: 終止所有指定的進程

## Overview
`killall` 命令用於終止所有符合指定名稱的進程。這是一個非常有用的工具，特別是在需要快速關閉多個相同進程的情況下。

## Usage
基本語法如下：
```
killall [選項] [進程名稱]
```

## Common Options
- `-u`：只終止指定用戶的進程。
- `-i`：在終止進程之前顯示確認提示。
- `-q`：靜默模式，不顯示錯誤信息。
- `-s`：指定要發送的信號（預設為 `TERM`）。

## Common Examples
1. 終止所有名為 `firefox` 的進程：
   ```bash
   killall firefox
   ```

2. 終止所有名為 `python` 的進程，並顯示確認提示：
   ```bash
   killall -i python
   ```

3. 終止所有名為 `myapp` 的進程，並使用 `SIGKILL` 信號：
   ```bash
   killall -s SIGKILL myapp
   ```

4. 終止指定用戶的所有 `ssh` 進程：
   ```bash
   killall -u username ssh
   ```

## Tips
- 使用 `-i` 選項可以避免意外終止重要進程。
- 在使用 `killall` 前，建議先用 `pgrep` 檢查進程是否存在。
- 確保你有足夠的權限來終止指定的進程，特別是當進程屬於其他用戶時。