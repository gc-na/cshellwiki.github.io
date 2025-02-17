# [台灣] Bash mkfs 使用法: 格式化檔案系統

## Overview
`mkfs` 命令用於創建檔案系統，通常在磁碟或分割區上進行格式化，以便可以存儲資料。這是管理檔案系統的基本工具之一。

## Usage
基本語法如下：
```bash
mkfs [選項] [參數]
```

## Common Options
- `-t`：指定檔案系統類型，例如 ext4、vfat 等。
- `-L`：為檔案系統指定一個標籤。
- `-n`：不進行格式化，只顯示將要執行的命令。
- `-V`：顯示版本資訊。

## Common Examples
1. 格式化一個 ext4 檔案系統：
   ```bash
   mkfs -t ext4 /dev/sdb1
   ```

2. 格式化一個 vfat 檔案系統並設定標籤：
   ```bash
   mkfs -t vfat -L MY_USB /dev/sdc1
   ```

3. 顯示將要執行的 mkfs 命令：
   ```bash
   mkfs -n -t ext4 /dev/sdb1
   ```

4. 格式化一個檔案系統並顯示版本：
   ```bash
   mkfs -V -t ext4 /dev/sdb1
   ```

## Tips
- 在執行 `mkfs` 前，請確保備份重要資料，因為格式化會刪除所有資料。
- 使用 `-n` 選項可以幫助你確認命令的正確性，避免意外格式化錯誤的磁碟。
- 確保你有適當的權限來執行 `mkfs`，通常需要以 root 身份執行。