# [Linux] Bash vgcreate 使用法: 創建邏輯卷組

## Overview
`vgcreate` 是一個用於創建邏輯卷組（Volume Group, VG）的命令。它是 Linux 磁碟管理的一部分，通常與 LVM（邏輯卷管理）一起使用，允許用戶將多個物理磁碟合併成一個邏輯卷組，從而更靈活地管理儲存空間。

## Usage
基本語法如下：
```bash
vgcreate [options] [vg_name] [physical_volume...]
```

## Common Options
- `-s, --stripes <n>`: 設定邏輯卷的條帶數量。
- `-p, --stripesize <n>`: 設定條帶大小。
- `-A, --activate`：在創建後立即啟用邏輯卷組。
- `-d, --debug`：啟用調試模式，顯示詳細的執行過程。

## Common Examples
1. 創建一個名為 `vg01` 的邏輯卷組，並將 `/dev/sda1` 和 `/dev/sdb1` 作為物理卷：
   ```bash
   vgcreate vg01 /dev/sda1 /dev/sdb1
   ```

2. 創建一個名為 `vg_data` 的邏輯卷組，並指定條帶數量為 2：
   ```bash
   vgcreate -s 2 vg_data /dev/sdc1
   ```

3. 創建一個邏輯卷組並立即啟用：
   ```bash
   vgcreate -A y vg_active /dev/sdd1
   ```

## Tips
- 在創建邏輯卷組之前，確保所使用的物理卷已經初始化並可用。
- 使用 `vgdisplay` 命令檢查已創建的邏輯卷組的狀態。
- 定期備份邏輯卷組的配置，以防數據丟失。