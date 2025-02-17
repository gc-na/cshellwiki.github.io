# [Linux] Bash lvextend 用法: 擴展邏輯卷的大小

## Overview
`lvextend` 是一個用於擴展邏輯卷大小的命令。它允許用戶增加邏輯卷的容量，以便能夠存儲更多的數據。

## Usage
基本語法如下：
```bash
lvextend [options] [arguments]
```

## Common Options
- `-L +size`：增加邏輯卷的大小，`size` 可以是 KB、MB、GB 等單位。
- `-l +number`：根據邏輯卷的邏輯區塊數量來增加大小。
- `-r`：在擴展邏輯卷後，自動調整文件系統的大小。
- `-n`：指定邏輯卷的名稱。

## Common Examples
以下是一些常見的使用範例：

1. 增加邏輯卷的大小 10GB：
   ```bash
   lvextend -L +10G /dev/vg_name/lv_name
   ```

2. 根據邏輯區塊數量增加大小：
   ```bash
   lvextend -l +100 /dev/vg_name/lv_name
   ```

3. 同時擴展邏輯卷並調整文件系統大小：
   ```bash
   lvextend -r -L +5G /dev/vg_name/lv_name
   ```

4. 指定新的邏輯卷名稱：
   ```bash
   lvextend -n new_lv_name /dev/vg_name/lv_name
   ```

## Tips
- 在執行 `lvextend` 之前，建議先備份重要數據，以防意外情況發生。
- 使用 `-r` 選項可以簡化流程，避免手動調整文件系統。
- 確保在擴展邏輯卷之前，物理卷有足夠的空間可用。