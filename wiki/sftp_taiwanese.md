# [台灣] Bash sftp 使用方式: 安全檔案傳輸

## Overview
`sftp`（安全檔案傳輸協定）是一種用於在網路上安全地傳輸檔案的命令行工具。它基於SSH協定，提供加密的檔案傳輸功能，確保資料的安全性。

## Usage
基本語法如下：
```bash
sftp [options] [user@]host
```

## Common Options
- `-P`：指定連接的端口號。
- `-o`：用來指定SSH選項，例如 `-o StrictHostKeyChecking=no`。
- `-b`：使用批次模式，從檔案中讀取命令。
- `-v`：啟用詳細模式，顯示更多的連接資訊。

## Common Examples
以下是一些常見的 `sftp` 使用範例：

1. 連接到遠端伺服器：
   ```bash
   sftp user@example.com
   ```

2. 指定端口連接：
   ```bash
   sftp -P 2222 user@example.com
   ```

3. 上傳檔案到遠端伺服器：
   ```bash
   sftp user@example.com
   put localfile.txt
   ```

4. 下載檔案到本地：
   ```bash
   sftp user@example.com
   get remotefile.txt
   ```

5. 使用批次模式上傳多個檔案：
   ```bash
   sftp -b batchfile.txt user@example.com
   ```

## Tips
- 在使用 `sftp` 時，確保你有正確的使用者名稱和密碼，或是使用SSH金鑰來進行無密碼登入。
- 使用 `-v` 選項可以幫助你排除連接問題。
- 定期檢查你的SSH金鑰和連接設定，以確保安全性。