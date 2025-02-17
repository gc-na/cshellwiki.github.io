# [Linux] Bash groups 使用方式: 查詢使用者所屬群組

## Overview
`groups` 命令用於顯示當前使用者或指定使用者所屬的群組。這對於管理使用者權限和了解系統中的群組結構非常有用。

## Usage
基本語法如下：
```
groups [options] [arguments]
```

## Common Options
- `-h`, `--help`: 顯示幫助信息。
- `-v`, `--version`: 顯示版本信息。

## Common Examples
1. **查詢當前使用者的群組**：
   ```bash
   groups
   ```

2. **查詢指定使用者的群組**：
   ```bash
   groups username
   ```

3. **查詢多個使用者的群組**：
   ```bash
   groups user1 user2
   ```

## Tips
- 使用 `groups` 命令時，若不指定使用者，系統會自動查詢當前登入的使用者。
- 了解使用者所屬的群組可以幫助你更好地管理文件和資料夾的權限。