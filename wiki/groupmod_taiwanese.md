# [台灣] Bash groupmod 使用法: 修改群組的屬性

## Overview
`groupmod` 命令用於修改現有群組的屬性，例如群組名稱或群組的 GID（群組識別碼）。

## Usage
基本語法如下：
```
groupmod [選項] [參數]
```

## Common Options
- `-n, --new-name <新名稱>`: 將群組名稱更改為指定的新名稱。
- `-g, --gid <新 GID>`: 將群組的 GID 更改為指定的新 GID。
- `-h, --help`: 顯示幫助信息。

## Common Examples
1. 更改群組名稱：
   ```bash
   groupmod -n newgroup oldgroup
   ```

2. 更改群組的 GID：
   ```bash
   groupmod -g 1001 groupname
   ```

3. 同時更改群組名稱和 GID：
   ```bash
   groupmod -n newgroup -g 1002 oldgroup
   ```

## Tips
- 在更改群組名稱或 GID 之前，確保沒有其他用戶正在使用該群組，以避免權限問題。
- 使用 `getent group` 命令檢查群組的當前設置，以便在修改之前了解其狀態。
- 在進行重大更改之前，建議備份系統的群組文件，以防出現意外情況。