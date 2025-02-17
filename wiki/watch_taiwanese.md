# [Linux] Bash watch 使用法: 監控命令輸出

## Overview
`watch` 命令用於定期執行指定的命令，並在終端中顯示其輸出。這對於需要持續監控某個命令的結果非常有用，例如查看系統資源使用情況或文件變更。

## Usage
基本語法如下：
```
watch [options] [arguments]
```

## Common Options
- `-n, --interval`: 設定每次執行命令的間隔時間（以秒為單位）。
- `-d, --differences`: 高亮顯示輸出中的差異。
- `-t, --no-title`: 不顯示標題行。
- `-p, --precise`: 提供更精確的時間間隔。

## Common Examples
1. 每2秒執行 `date` 命令，顯示當前時間：
   ```bash
   watch -n 2 date
   ```

2. 監控 `/var/log/syslog` 文件的變更，每1秒更新一次：
   ```bash
   watch -n 1 tail -n 10 /var/log/syslog
   ```

3. 每5秒檢查系統的磁碟使用情況：
   ```bash
   watch -n 5 df -h
   ```

4. 使用 `-d` 選項高亮顯示變更的 `ps` 命令輸出：
   ```bash
   watch -d ps aux
   ```

## Tips
- 使用 `-t` 選項可以讓界面更乾淨，適合不需要標題的情況。
- 結合 `-d` 和 `-n` 可以更有效地監控變化，尤其是在頻繁變化的環境中。
- 若要停止 `watch`，可以按下 `Ctrl+C`。