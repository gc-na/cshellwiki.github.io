# [Linux] Bash vipw 用法: 編輯密碼檔案

## Overview
`vipw` 命令用於安全地編輯系統的密碼檔案（/etc/passwd 和 /etc/shadow）。它確保在編輯過程中不會有其他進程修改這些檔案，從而避免潛在的數據損壞。

## Usage
基本語法如下：
```bash
vipw [options]
```

## Common Options
- `-s`：編輯 `/etc/shadow` 檔案。
- `-u`：指定要編輯的使用者名稱。
- `-g`：指定要編輯的群組名稱。

## Common Examples
1. 編輯密碼檔案：
   ```bash
   vipw
   ```

2. 編輯影子檔案：
   ```bash
   vipw -s
   ```

3. 編輯特定使用者的資訊：
   ```bash
   vipw -u username
   ```

## Tips
- 在使用 `vipw` 編輯檔案之前，建議先備份相關的密碼檔案，以防止意外損壞。
- 使用 `vipw` 時，請確保您擁有適當的權限，通常需要以 root 身份執行。
- 編輯完成後，檢查檔案的格式和內容，確保沒有語法錯誤，以避免系統登入問題。