# [Linux] Bash umask 使用法: 設定預設檔案權限

## Overview
`umask` 命令用來設定新建立檔案和目錄的預設權限掩碼。這個掩碼決定了檔案和目錄的預設可讀、可寫和可執行權限。

## Usage
基本語法如下：
```
umask [options] [arguments]
```

## Common Options
- `-S`：以符號形式顯示當前的 umask 值。
- `-p`：顯示當前的 umask 值，並且不會改變它。

## Common Examples
1. **查看當前 umask 值**
   ```bash
   umask
   ```

2. **設定 umask 值為 022**
   ```bash
   umask 022
   ```
   這將使新建立的檔案預設為可讀取，但不可寫入，目錄則可讀取和可執行。

3. **以符號形式顯示 umask 值**
   ```bash
   umask -S
   ```

4. **設定 umask 值為 007**
   ```bash
   umask 007
   ```
   這將使新檔案和目錄對其他用戶不可見。

## Tips
- 在設定 umask 時，建議使用數字形式，因為這樣更直觀且不易出錯。
- 為了安全起見，對於公共或共享系統，建議將 umask 設定為 027 或 007，以限制其他用戶的訪問權限。
- 可以將 umask 設定放入使用者的啟動檔案（如 `.bashrc` 或 `.bash_profile`），以便每次登入時自動應用。