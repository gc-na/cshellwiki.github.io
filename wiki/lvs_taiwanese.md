# [Linux] Bash lvs 使用法: 顯示邏輯卷資訊

## Overview
`lvs` 命令用於顯示邏輯卷的資訊，這是 LVM（邏輯卷管理）的一部分。透過這個命令，使用者可以快速查看系統中所有邏輯卷的狀態和屬性。

## Usage
基本語法如下：
```
lvs [options] [arguments]
```

## Common Options
- `-o`：指定要顯示的欄位。
- `-a`：顯示所有邏輯卷，包括隱藏的。
- `--units`：指定顯示的單位（例如：G、M）。
- `-n`：顯示邏輯卷的名稱。

## Common Examples
以下是一些常見的 `lvs` 使用範例：

1. 顯示所有邏輯卷的基本資訊：
   ```bash
   lvs
   ```

2. 顯示所有邏輯卷的詳細資訊，包括隱藏的邏輯卷：
   ```bash
   lvs -a
   ```

3. 顯示特定欄位的邏輯卷資訊，例如名稱和大小：
   ```bash
   lvs -o lv_name,lv_size
   ```

4. 使用指定單位顯示邏輯卷大小：
   ```bash
   lvs --units g
   ```

5. 顯示特定邏輯卷的資訊：
   ```bash
   lvs my_volume_group/my_logical_volume
   ```

## Tips
- 在使用 `lvs` 時，可以結合其他 LVM 命令，例如 `vgdisplay` 和 `pvdisplay`，以獲得更全面的存儲資訊。
- 定期檢查邏輯卷的狀態，以確保系統的穩定性和性能。
- 使用 `-o` 選項來自定義顯示的資訊，這樣可以更方便地獲取所需的數據。