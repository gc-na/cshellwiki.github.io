# [Linux] Bash mountpoint 用法: 檢查檔案系統掛載點

## Overview
`mountpoint` 命令用於檢查指定的目錄是否為一個掛載點。這在管理檔案系統和確保正確的掛載狀態時非常有用。

## Usage
基本語法如下：
```
mountpoint [選項] [參數]
```

## Common Options
- `-q`: 靜默模式，無輸出。
- `-d`: 顯示詳細信息，包括掛載的檔案系統類型。

## Common Examples
1. 檢查某個目錄是否為掛載點：
   ```bash
   mountpoint /mnt/mydrive
   ```

2. 使用靜默模式檢查掛載點：
   ```bash
   mountpoint -q /mnt/mydrive
   ```

3. 顯示詳細信息：
   ```bash
   mountpoint -d /mnt/mydrive
   ```

## Tips
- 在使用 `mountpoint` 前，確保你有足夠的權限來訪問指定的目錄。
- 可以將 `mountpoint` 與其他命令結合使用，以自動化檢查和掛載流程。