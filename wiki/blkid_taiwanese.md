# [Linux] Bash blkid 用法: 查詢磁碟區的 UUID 和檔案系統類型

## Overview
`blkid` 是一個用於查詢和顯示區塊設備（例如硬碟、USB 隨身碟等）相關資訊的命令。它可以顯示每個設備的 UUID、檔案系統類型和其他相關屬性。

## Usage
基本語法如下：
```
blkid [options] [arguments]
```

## Common Options
- `-o, --output`: 指定輸出格式，例如 `value` 或 `full`。
- `-s, --match-tag`: 只顯示特定標籤的資訊。
- `-p, --probe`: 探測設備的檔案系統類型。
- `-c, --cache`: 使用快取來加速查詢。

## Common Examples
1. 查詢所有區塊設備的 UUID 和檔案系統類型：
   ```bash
   blkid
   ```

2. 查詢特定設備的 UUID：
   ```bash
   blkid /dev/sda1
   ```

3. 以 `value` 格式輸出 UUID：
   ```bash
   blkid -o value -s UUID /dev/sda1
   ```

4. 只顯示特定標籤的資訊：
   ```bash
   blkid -s TYPE
   ```

## Tips
- 使用 `sudo` 來獲取更完整的設備資訊，因為某些設備可能需要管理員權限才能訪問。
- 定期檢查設備的 UUID，特別是在進行系統備份或恢復時，這樣可以確保正確的設備被掛載。
- 結合 `grep` 使用，可以更方便地過濾出所需的資訊，例如：
  ```bash
  blkid | grep sda
  ```