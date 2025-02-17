# [Linux] Bash lsblk 使用方法: 列出區塊設備

## Overview
`lsblk` 是一個用於列出系統中所有區塊設備的命令。它顯示了設備的層級結構，包括硬碟、分割區、以及其他存儲設備，幫助用戶了解系統的存儲配置。

## Usage
基本語法如下：
```
lsblk [options] [arguments]
```

## Common Options
- `-a` 或 `--all`: 顯示所有設備，包括沒有掛載的設備。
- `-f` 或 `--fs`: 顯示文件系統的相關信息。
- `-l` 或 `--list`: 以列表形式顯示設備，而不是樹狀結構。
- `-o` 或 `--output`: 自訂輸出的欄位，例如 `NAME,SIZE,TYPE,MOUNTPOINT`。
- `-n` 或 `--noheadings`: 不顯示標題行。

## Common Examples
1. 列出所有區塊設備：
   ```bash
   lsblk
   ```

2. 顯示所有設備的詳細信息，包括文件系統：
   ```bash
   lsblk -f
   ```

3. 以列表形式顯示設備：
   ```bash
   lsblk -l
   ```

4. 自訂輸出顯示的欄位：
   ```bash
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

5. 顯示所有設備，包括未掛載的設備：
   ```bash
   lsblk -a
   ```

## Tips
- 使用 `lsblk -f` 可以快速檢查設備的文件系統類型，這對於管理存儲設備非常有幫助。
- 結合 `grep` 使用，可以快速找到特定的設備，例如：
  ```bash
  lsblk | grep sda
  ```
- 定期檢查區塊設備的狀態，特別是在進行系統維護或升級時，能幫助避免潛在的問題。