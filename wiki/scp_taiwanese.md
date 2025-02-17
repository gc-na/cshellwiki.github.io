# [台灣] Bash scp 使用方式: 用於安全地複製檔案

## Overview
`scp`（Secure Copy Protocol）是一個用於在本地和遠端主機之間安全地複製檔案的命令。它使用SSH協議來加密傳輸過程，確保資料的安全性。

## Usage
基本語法如下：
```
scp [選項] [來源] [目標]
```

## Common Options
- `-r`: 遞迴複製整個目錄。
- `-P`: 指定遠端主機的端口號（注意是大寫的P）。
- `-i`: 指定用於身份驗證的私鑰檔案。
- `-v`: 顯示詳細的執行過程，方便除錯。

## Common Examples
1. 複製本地檔案到遠端主機：
   ```bash
   scp /path/to/local/file username@remote_host:/path/to/remote/directory/
   ```

2. 從遠端主機複製檔案到本地：
   ```bash
   scp username@remote_host:/path/to/remote/file /path/to/local/directory/
   ```

3. 遞迴複製整個目錄到遠端主機：
   ```bash
   scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory/
   ```

4. 使用自定義端口複製檔案：
   ```bash
   scp -P 2222 /path/to/local/file username@remote_host:/path/to/remote/directory/
   ```

## Tips
- 確保SSH服務在遠端主機上運行，這樣才能使用`scp`命令。
- 使用`-v`選項來檢查連接問題或身份驗證錯誤。
- 在複製大量檔案時，可以考慮使用`rsync`，因為它在增量複製時更有效率。