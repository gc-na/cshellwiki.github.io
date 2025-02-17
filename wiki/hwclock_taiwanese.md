# [Linux] Bash hwclock 用法: 設定和查詢硬體時鐘

## Overview
`hwclock` 命令用於查詢和設定系統的硬體時鐘。硬體時鐘是獨立於操作系統的時鐘，通常在系統關機時仍然保持運行。

## Usage
基本語法如下：
```
hwclock [options] [arguments]
```

## Common Options
- `--show`：顯示當前的硬體時鐘時間。
- `--set`：設定硬體時鐘的時間。
- `--hctosys`：將硬體時鐘的時間設置為系統時間。
- `--systohc`：將系統時間設置為硬體時鐘的時間。
- `--utc`：以協調世界時間（UTC）格式顯示或設定時間。

## Common Examples
- 顯示當前的硬體時鐘時間：
  ```bash
  hwclock --show
  ```

- 將系統時間設置為硬體時鐘的時間：
  ```bash
  hwclock --hctosys
  ```

- 將硬體時鐘的時間設置為當前系統時間：
  ```bash
  hwclock --systohc
  ```

- 設定硬體時鐘為特定時間（例如：2023年10月1日 12:00:00）：
  ```bash
  hwclock --set --date="2023-10-01 12:00:00"
  ```

- 以UTC格式顯示硬體時鐘時間：
  ```bash
  hwclock --utc --show
  ```

## Tips
- 確保在設定硬體時鐘之前，系統時間是正確的，以避免時間不一致的問題。
- 定期檢查硬體時鐘，以確保其準確性，特別是在使用虛擬機或多重啟動系統時。
- 使用 `--utc` 選項可以避免時區問題，特別是在伺服器環境中。