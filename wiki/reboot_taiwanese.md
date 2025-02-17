# [Linux] Bash reboot 使用方式: 重新啟動系統

## Overview
`reboot` 命令用於重新啟動系統。當你需要重啟伺服器或工作站以應用更新或解決問題時，這個命令非常有用。

## Usage
基本語法如下：
```
reboot [options] [arguments]
```

## Common Options
- `-f`：強制重啟，不執行正常的關閉程序。
- `-i`：在重啟前發送中斷信號。
- `-p`：在重啟後關閉電源（如果支援）。

## Common Examples
1. **正常重啟系統**
   ```bash
   reboot
   ```

2. **強制重啟系統**
   ```bash
   reboot -f
   ```

3. **重啟並關閉電源**
   ```bash
   reboot -p
   ```

4. **使用 `shutdown` 命令進行重啟**
   ```bash
   shutdown -r now
   ```

## Tips
- 在使用 `reboot` 前，確保所有重要的工作已儲存，以免資料遺失。
- 使用 `-f` 選項時要小心，因為這會跳過正常的關閉程序，可能導致資料損壞。
- 定期重啟系統可以幫助清理記憶體和應用更新，保持系統穩定。