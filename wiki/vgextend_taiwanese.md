# [Linux] Bash vgextend 用法: 擴展邏輯卷組

## Overview
`vgextend` 是一個用於擴展邏輯卷組的命令。當你需要將新的物理卷添加到現有的邏輯卷組時，可以使用此命令來增加可用的存儲空間。

## Usage
基本語法如下：
```bash
vgextend [options] [arguments]
```

## Common Options
- `-f`：強制執行擴展，即使有錯誤也不會停止。
- `--test`：執行測試，不會實際改變任何內容。
- `-n`：指定要添加的物理卷的名稱。

## Common Examples
1. 將物理卷 `/dev/sdb1` 添加到邏輯卷組 `vg01`：
   ```bash
   vgextend vg01 /dev/sdb1
   ```

2. 強制將物理卷 `/dev/sdc1` 添加到邏輯卷組 `vg02`：
   ```bash
   vgextend -f vg02 /dev/sdc1
   ```

3. 測試將物理卷 `/dev/sdd1` 添加到邏輯卷組 `vg03`：
   ```bash
   vgextend --test vg03 /dev/sdd1
   ```

## Tips
- 在執行 `vgextend` 之前，建議先使用 `pvcreate` 命令初始化物理卷。
- 確保在擴展邏輯卷組之前，檢查物理卷的狀態，避免因為錯誤的物理卷導致擴展失敗。
- 使用 `vgs` 命令檢查邏輯卷組的狀態和可用空間，以便做出更好的決策。