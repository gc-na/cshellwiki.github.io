# [Linux] Bash update-rc.d 使用法: 管理系統服務啟動

## Overview
`update-rc.d` 是一個用於管理系統服務啟動的命令，主要用於在 Debian 和 Ubuntu 系統中添加、刪除或更新服務的啟動腳本。

## Usage
基本語法如下：
```
update-rc.d [options] [arguments]
```

## Common Options
- `defaults`：使用預設的啟動和停止優先級來添加服務。
- `remove`：從啟動序列中移除指定的服務。
- `enable`：啟用指定的服務，使其在啟動時自動運行。
- `disable`：禁用指定的服務，使其在啟動時不自動運行。

## Common Examples
以下是一些實用的範例：

1. **添加服務到啟動序列**
   ```bash
   sudo update-rc.d myservice defaults
   ```

2. **移除服務**
   ```bash
   sudo update-rc.d myservice remove
   ```

3. **啟用服務**
   ```bash
   sudo update-rc.d myservice enable
   ```

4. **禁用服務**
   ```bash
   sudo update-rc.d myservice disable
   ```

## Tips
- 確保在執行 `update-rc.d` 命令時擁有適當的管理權限，通常需要使用 `sudo`。
- 在添加或移除服務之前，建議先備份相關的啟動腳本，以防止意外刪除。
- 使用 `ls /etc/rc*.d/` 可以查看當前系統中所有的啟動服務。