# [Linux] Bash sysctl 使用法: 調整內核參數

## Overview
`sysctl` 命令用於在運行中的 Linux 系統上查詢和修改內核參數。這些參數影響系統的性能和行為，透過這個命令，使用者可以即時調整設定而無需重新啟動系統。

## Usage
基本語法如下：
```bash
sysctl [options] [arguments]
```

## Common Options
- `-a`：顯示所有可用的內核參數及其當前值。
- `-w`：用來修改內核參數的值。
- `-p`：從指定的檔案讀取參數設定，通常是 `/etc/sysctl.conf`。

## Common Examples
1. 查詢所有內核參數：
   ```bash
   sysctl -a
   ```

2. 修改某個內核參數，例如增加文件描述符的限制：
   ```bash
   sysctl -w fs.file-max=100000
   ```

3. 從配置檔案加載內核參數：
   ```bash
   sysctl -p
   ```

4. 查詢特定的內核參數，例如查看網路最大連接數：
   ```bash
   sysctl net.core.somaxconn
   ```

## Tips
- 在修改內核參數之前，建議先備份當前的設定，以便於恢復。
- 使用 `sysctl -p` 可以方便地應用配置檔中的所有設定，確保系統在啟動時使用正確的參數。
- 注意某些參數的修改可能會影響系統的穩定性，建議在生產環境中謹慎操作。