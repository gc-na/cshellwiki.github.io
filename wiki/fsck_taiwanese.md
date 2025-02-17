# [Linux] Bash fsck 使用法: 檢查檔案系統的完整性

## Overview
`fsck`（檔案系統檢查）是一個用於檢查和修復Linux及Unix系統中檔案系統的命令。它可以幫助用戶識別和修復檔案系統中的錯誤，確保資料的完整性和可用性。

## Usage
基本語法如下：
```bash
fsck [options] [arguments]
```

## Common Options
- `-a`：自動修復檔案系統錯誤。
- `-n`：不進行任何修復，只顯示錯誤。
- `-y`：自動回答“是”以修復所有檔案系統錯誤。
- `-t`：顯示執行時間。

## Common Examples
1. 檢查特定的檔案系統（例如 `/dev/sda1`）：
   ```bash
   fsck /dev/sda1
   ```

2. 自動修復檔案系統錯誤：
   ```bash
   fsck -a /dev/sda1
   ```

3. 只顯示錯誤而不進行修復：
   ```bash
   fsck -n /dev/sda1
   ```

4. 自動修復所有錯誤：
   ```bash
   fsck -y /dev/sda1
   ```

5. 檢查所有檔案系統（通常在啟動時使用）：
   ```bash
   fsck -A
   ```

## Tips
- 在執行 `fsck` 前，建議先備份重要資料，以防止資料損失。
- 避免在掛載的檔案系統上運行 `fsck`，最好在系統啟動時或進入單用戶模式下進行。
- 定期檢查檔案系統可以幫助及早發現問題，保持系統的穩定性。