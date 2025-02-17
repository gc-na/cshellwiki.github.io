# [Linux] Bash wait 使用法: 等待進程結束

## Overview
`wait` 命令用於等待一個或多個背景進程的結束。當你在 Bash 中啟動一個或多個進程時，使用 `wait` 可以讓你在繼續執行其他命令之前，確保這些進程已經完成。

## Usage
基本語法如下：
```bash
wait [options] [arguments]
```

## Common Options
- `-n`：等待下一個背景進程結束。
- `pid`：指定要等待的進程 ID。如果不指定，則等待所有背景進程結束。

## Common Examples
以下是一些常見的使用範例：

1. **等待所有背景進程結束**
   ```bash
   sleep 5 &
   sleep 3 &
   wait
   echo "所有背景進程已結束"
   ```

2. **等待特定進程結束**
   ```bash
   sleep 5 &
   pid=$!
   echo "等待進程 $pid 結束"
   wait $pid
   echo "進程 $pid 已結束"
   ```

3. **使用 -n 選項等待下一個進程**
   ```bash
   sleep 5 &
   sleep 3 &
   wait -n
   echo "下一個背景進程已結束"
   ```

## Tips
- 使用 `wait` 可以避免在背景進程未完成時執行後續命令，這對於需要依賴前一個進程結果的情況特別有用。
- 當你需要獲取背景進程的退出狀態時，可以將 `wait` 的返回值存入變數，例如 `status=$(wait $pid)`。
- 在腳本中使用 `wait` 可以提高可讀性，讓其他人更容易理解進程之間的依賴關係。