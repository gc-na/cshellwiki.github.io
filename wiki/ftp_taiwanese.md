# [台灣] Bash ftp 使用法: 傳輸檔案

## Overview
`ftp` 命令是一個用於在網路上傳輸檔案的工具，通常用於連接到 FTP 伺服器，並進行檔案的上傳和下載。

## Usage
基本語法如下：
```
ftp [options] [arguments]
```

## Common Options
- `-i`：關閉互動模式，適合批次傳輸。
- `-n`：不自動登入，需手動輸入登入資訊。
- `-v`：顯示詳細的傳輸過程。
- `-p`：使用被動模式連接，適合某些防火牆設定。

## Common Examples
以下是一些常見的 `ftp` 使用範例：

1. 連接到 FTP 伺服器：
   ```bash
   ftp ftp.example.com
   ```

2. 使用匿名登入：
   ```bash
   ftp -n ftp.example.com
   ```

3. 上傳檔案到伺服器：
   ```bash
   put localfile.txt
   ```

4. 下載檔案從伺服器：
   ```bash
   get remotefile.txt
   ```

5. 列出伺服器上的檔案：
   ```bash
   ls
   ```

## Tips
- 使用 `-i` 選項可以提高傳輸效率，特別是當需要上傳多個檔案時。
- 確保在傳輸敏感資料時使用安全的 FTP 變體，如 SFTP。
- 定期檢查 FTP 伺服器的連接狀態，以避免中斷傳輸。