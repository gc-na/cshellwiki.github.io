# [Linux] Bash write 使用方法: 發送即時訊息給其他使用者

## Overview
`write` 命令用於在 Linux 系統中向其他登入的使用者發送即時訊息。這個命令可以讓使用者在終端機中直接與其他使用者進行交流，適合在多使用者環境中使用。

## Usage
基本語法如下：
```
write [options] [user] [tty]
```
- `user`：接收訊息的使用者名稱。
- `tty`：接收訊息的終端機名稱（可選）。

## Common Options
- `-n`：不顯示接收者的名稱。
- `-s`：靜默模式，不顯示訊息的標頭。

## Common Examples
以下是一些常見的使用範例：

1. 向使用者 `alice` 發送訊息：
   ```bash
   write alice
   ```
   然後輸入要發送的訊息，按 `Ctrl+D` 結束。

2. 向使用者 `bob` 的特定終端機發送訊息：
   ```bash
   write bob pts/1
   ```

3. 使用靜默模式向使用者 `charlie` 發送訊息：
   ```bash
   write -s charlie
   ```

## Tips
- 確保接收者的終端機是開啟的，否則訊息將無法送達。
- 使用 `who` 命令可以查看當前登入的使用者及其終端機。
- 如果不想被打擾，可以使用 `mesg n` 命令來禁用接收訊息。