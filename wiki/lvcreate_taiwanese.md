# [Linux] Bash lvcreate 使用方法: 創建邏輯卷

## Overview
lvcreate 是一個用於在 Linux 系統中創建邏輯卷的命令。它是 LVM（邏輯卷管理）的一部分，允許用戶在物理卷上創建、調整和管理邏輯卷，從而更靈活地管理存儲空間。

## Usage
基本語法如下：
```bash
lvcreate [options] [arguments]
```

## Common Options
- `-n, --name <name>`: 指定邏輯卷的名稱。
- `-L, --size <size>`: 指定邏輯卷的大小。
- `-l, --extents <number>`: 指定邏輯卷的擴展數量。
- `-m, --mirrors <number>`: 指定邏輯卷的鏡像數量。
- `-Z, --zeroing <y/n>`: 指定是否在創建邏輯卷時清零。

## Common Examples
1. 創建一個名為 `my_volume` 的邏輯卷，大小為 10G：
   ```bash
   lvcreate -n my_volume -L 10G my_volume_group
   ```

2. 創建一個大小為 5G 的邏輯卷，並在創建時清零：
   ```bash
   lvcreate -n my_zeroed_volume -L 5G -Z y my_volume_group
   ```

3. 創建一個邏輯卷，指定使用擴展數量：
   ```bash
   lvcreate -n my_extent_volume -l 100 my_volume_group
   ```

4. 創建一個具有 2 個鏡像的邏輯卷：
   ```bash
   lvcreate -n my_mirrored_volume -m 2 -L 20G my_volume_group
   ```

## Tips
- 在創建邏輯卷之前，確保已經有可用的物理卷和卷組。
- 使用 `lvdisplay` 命令檢查已創建的邏輯卷及其屬性。
- 考慮使用 `-Z y` 選項來清零新邏輯卷，以提高數據安全性。