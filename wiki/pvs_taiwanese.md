# [Linux] Bash pvs 使用法: 顯示邏輯卷的狀態

## Overview
`pvs` 命令用於顯示邏輯卷管理器（LVM）中的物理卷資訊。它提供了有關物理卷的詳細狀態，包括其大小、使用情況和屬性等。

## Usage
基本語法如下：
```
pvs [options] [arguments]
```

## Common Options
- `-o, --options`: 指定要顯示的欄位。
- `--units`: 設定輸出單位，例如 MB 或 GB。
- `-a, --all`: 顯示所有物理卷，包括未啟用的。
- `-h, --help`: 顯示幫助信息。

## Common Examples
1. 顯示所有物理卷的基本資訊：
   ```bash
   pvs
   ```

2. 顯示所有物理卷的詳細資訊，包括使用情況：
   ```bash
   pvs -o +pv_used
   ```

3. 使用特定單位顯示物理卷大小：
   ```bash
   pvs --units g
   ```

4. 顯示所有物理卷，包括未啟用的：
   ```bash
   pvs -a
   ```

## Tips
- 使用 `-o` 選項可以自定義輸出，選擇最相關的欄位來顯示。
- 定期檢查物理卷的狀態，以確保 LVM 的健康運行。
- 結合其他 LVM 命令（如 `lvdisplay` 和 `vgdisplay`）使用，可以獲得更全面的系統狀態資訊。