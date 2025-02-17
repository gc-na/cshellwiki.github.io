# [Linux] Bash mount 使用法: 挂载文件系统

## Overview
`mount` 命令用於將文件系統掛載到 Linux 系統中的某個目錄。這使得用戶可以訪問和管理不同的存儲設備或分區中的文件。

## Usage
基本語法如下：
```
mount [options] [arguments]
```

## Common Options
- `-t`：指定文件系統類型，例如 `ext4`、`ntfs` 等。
- `-o`：用於指定掛載選項，如 `ro`（只讀）或 `rw`（讀寫）。
- `-a`：掛載 `/etc/fstab` 文件中列出的所有文件系統。
- `-r`：以只讀模式掛載文件系統。

## Common Examples
1. **掛載一個 USB 驅動器**
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. **以只讀模式掛載一個分區**
   ```bash
   mount -o ro /dev/sda1 /mnt/data
   ```

3. **掛載所有在 fstab 中定義的文件系統**
   ```bash
   mount -a
   ```

4. **掛載一個 NTFS 文件系統**
   ```bash
   mount -t ntfs-3g /dev/sdc1 /mnt/ntfs
   ```

## Tips
- 確保在掛載之前，目錄已經存在，否則會出現錯誤。
- 使用 `umount` 命令來卸載已掛載的文件系統。
- 檢查 `/etc/fstab` 文件，以便自動掛載文件系統。