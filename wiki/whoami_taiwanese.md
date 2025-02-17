# [Linux] Bash whoami 用法: 顯示當前使用者名稱

## Overview
`whoami` 命令用於顯示當前登錄的使用者名稱。這是一個簡單而有效的命令，特別是在多用戶系統中，幫助用戶確認他們的身份。

## Usage
基本語法如下：

```bash
whoami [options]
```

## Common Options
`whoami` 命令通常不需要選項，但以下是一些常見的選項：

- `--help`：顯示幫助信息。
- `--version`：顯示版本信息。

## Common Examples
以下是一些常見的使用範例：

1. 顯示當前使用者名稱：
   ```bash
   whoami
   ```

2. 顯示幫助信息：
   ```bash
   whoami --help
   ```

3. 顯示版本信息：
   ```bash
   whoami --version
   ```

## Tips
- 在腳本中使用 `whoami` 可以幫助確認腳本是以哪個使用者身份執行的。
- 如果你在使用 sudo 命令後想確認當前使用者，可以再次執行 `whoami` 來檢查。
- `whoami` 是一個輕量級的命令，適合在需要快速確認使用者身份的情況下使用。