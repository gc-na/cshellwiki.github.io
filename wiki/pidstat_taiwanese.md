# [台灣] Bash pidstat 使用說明: 監控進程統計資訊

## Overview
`pidstat` 是一個用於監控系統中各個進程的性能統計工具。它可以顯示每個進程的 CPU 使用率、記憶體使用情況和其他性能指標，對於系統管理員和開發者來說非常有用。

## Usage
基本語法如下：
```
pidstat [選項] [參數]
```

## Common Options
- `-h`：顯示幫助信息。
- `-r`：顯示記憶體使用情況。
- `-u`：顯示 CPU 使用率。
- `-p <pid>`：指定要監控的進程 ID。
- `-t`：顯示每個進程的執行緒統計。

## Common Examples
以下是一些常見的使用範例：

1. 監控所有進程的 CPU 使用率：
   ```bash
   pidstat -u 1
   ```

2. 監控特定進程（例如 PID 1234）的記憶體使用情況：
   ```bash
   pidstat -r -p 1234 1
   ```

3. 每 2 秒顯示一次所有進程的 CPU 和記憶體使用情況：
   ```bash
   pidstat -u -r 2
   ```

4. 監控所有進程的執行緒統計：
   ```bash
   pidstat -t 1
   ```

## Tips
- 使用 `-h` 選項來獲取幫助信息，了解更多可用選項。
- 結合 `grep` 命令來過濾特定進程的輸出，例如：
  ```bash
  pidstat -u 1 | grep <process_name>
  ```
- 定期監控系統性能，幫助及早發現潛在問題。