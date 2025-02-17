# [Linux] Bash id 使用法: 查詢使用者身份資訊

## Overview
`id` 命令用來顯示當前使用者或指定使用者的身份資訊，包括使用者的 UID（使用者識別碼）、GID（群組識別碼）以及所屬的群組列表。

## Usage
基本語法如下：
```bash
id [options] [username]
```

## Common Options
- `-u`: 顯示使用者的 UID。
- `-g`: 顯示使用者的 GID。
- `-G`: 顯示使用者所屬的所有群組的 GID。
- `-n`: 以名稱顯示 UID 或 GID，而不是數字。

## Common Examples
1. 顯示當前使用者的身份資訊：
   ```bash
   id
   ```

2. 顯示指定使用者的身份資訊：
   ```bash
   id username
   ```

3. 只顯示當前使用者的 UID：
   ```bash
   id -u
   ```

4. 只顯示當前使用者的 GID：
   ```bash
   id -g
   ```

5. 顯示當前使用者所屬的所有群組的 GID：
   ```bash
   id -G
   ```

6. 以名稱顯示指定使用者的 UID 和 GID：
   ```bash
   id -n username
   ```

## Tips
- 使用 `id` 命令可以快速確認使用者的權限和所屬群組，對於管理系統非常有幫助。
- 當需要檢查某個使用者的身份資訊時，記得使用 `id username`，這樣可以避免混淆當前使用者的資訊。