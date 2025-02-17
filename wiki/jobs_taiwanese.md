# [Linux] Bash jobs 使用方法: 管理背景工作

## Overview
`jobs` 命令用來顯示當前 shell 中的所有背景工作。它可以幫助用戶查看正在運行的進程，以及它們的狀態（例如，運行中、停止等）。

## Usage
基本語法如下：
```
jobs [options] [arguments]
```

## Common Options
- `-l`：顯示每個工作對應的進程 ID（PID）。
- `-n`：僅顯示最近狀態改變的工作。
- `-p`：僅顯示工作對應的進程 ID。

## Common Examples
以下是一些常見的使用範例：

1. 顯示所有背景工作：
   ```bash
   jobs
   ```

2. 顯示背景工作及其進程 ID：
   ```bash
   jobs -l
   ```

3. 僅顯示最近狀態改變的工作：
   ```bash
   jobs -n
   ```

4. 僅顯示進程 ID：
   ```bash
   jobs -p
   ```

## Tips
- 在使用 `jobs` 命令之前，確保你有一些背景工作正在運行，這樣你才能看到相關的輸出。
- 結合 `fg` 和 `bg` 命令，可以更有效地管理你的背景工作，例如將某個工作帶回前景或繼續在背景中運行。