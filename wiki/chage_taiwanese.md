# [Linux] Bash chage 使用法: 管理使用者密碼有效期限

## Overview
`chage` 命令用於管理 Linux 系統中使用者的密碼有效期限。它可以設定密碼的過期時間、最小使用期限以及警告使用者密碼即將到期的時間。

## Usage
基本語法如下：
```bash
chage [選項] [參數]
```

## Common Options
- `-l, --list`: 列出指定使用者的密碼過期資訊。
- `-m, --mindays`: 設定密碼的最小使用天數。
- `-M, --maxdays`: 設定密碼的最大使用天數。
- `-I, --inactive`: 設定密碼過期後的非活動天數。
- `-W, --warndays`: 設定在密碼過期前幾天開始警告使用者。

## Common Examples
1. 列出使用者的密碼過期資訊：
   ```bash
   chage -l username
   ```

2. 設定密碼的最小使用天數為 7 天：
   ```bash
   chage -m 7 username
   ```

3. 設定密碼的最大使用天數為 90 天：
   ```bash
   chage -M 90 username
   ```

4. 設定密碼過期後的非活動天數為 30 天：
   ```bash
   chage -I 30 username
   ```

5. 設定在密碼過期前 14 天開始警告使用者：
   ```bash
   chage -W 14 username
   ```

## Tips
- 確保在設定密碼過期策略時，考慮到使用者的需求，避免造成不必要的困擾。
- 定期檢查使用者的密碼過期設定，以保持系統的安全性。
- 使用 `chage -l username` 命令來確認設定是否正確。