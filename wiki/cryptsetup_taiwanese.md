# [Linux] Bash cryptsetup 使用法: 加密磁碟的工具

## Overview
`cryptsetup` 是一個用於管理 Linux 磁碟加密的工具，特別是用於設置和管理 LUKS（Linux Unified Key Setup）加密。它可以幫助用戶保護敏感資料，確保資料在未經授權的情況下無法訪問。

## Usage
基本語法如下：
```
cryptsetup [options] [arguments]
```

## Common Options
- `luksFormat`：將指定的裝置格式化為 LUKS 加密格式。
- `luksOpen`：打開 LUKS 加密的裝置，並將其映射到一個虛擬裝置。
- `luksClose`：關閉先前打開的 LUKS 裝置。
- `status`：顯示加密裝置的狀態。
- `luksAddKey`：為 LUKS 裝置添加一個新的密碼。

## Common Examples
1. **格式化一個裝置為 LUKS 加密**：
   ```bash
   cryptsetup luksFormat /dev/sdX
   ```

2. **打開 LUKS 加密的裝置**：
   ```bash
   cryptsetup luksOpen /dev/sdX my_encrypted_volume
   ```

3. **關閉 LUKS 裝置**：
   ```bash
   cryptsetup luksClose my_encrypted_volume
   ```

4. **檢查加密裝置的狀態**：
   ```bash
   cryptsetup status my_encrypted_volume
   ```

5. **為 LUKS 裝置添加新的密碼**：
   ```bash
   cryptsetup luksAddKey /dev/sdX
   ```

## Tips
- 在使用 `luksFormat` 前，請確保備份重要資料，因為這將清除裝置上的所有資料。
- 使用強密碼來保護加密裝置，避免使用容易猜測的密碼。
- 定期檢查加密裝置的狀態，確保其正常運作。