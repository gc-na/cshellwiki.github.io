# [Linux] Bash insmod 使用法: 載入內核模組

## Overview
`insmod` 是一個用於 Linux 系統的命令，用來將內核模組載入到正在運行的 Linux 內核中。這個命令通常用於添加新的功能或驅動程式，讓系統能夠支持新的硬體或功能。

## Usage
基本語法如下：
```
insmod [選項] [模組檔案]
```

## Common Options
- `-f`：強制載入模組，即使有錯誤。
- `-v`：顯示詳細的載入過程。
- `--dry-run`：模擬載入過程，但不實際執行。

## Common Examples
1. 載入一個名為 `example.ko` 的模組：
   ```bash
   insmod example.ko
   ```

2. 使用詳細模式載入模組：
   ```bash
   insmod -v example.ko
   ```

3. 強制載入模組，即使有錯誤：
   ```bash
   insmod -f example.ko
   ```

4. 模擬載入過程：
   ```bash
   insmod --dry-run example.ko
   ```

## Tips
- 確保模組檔案的路徑正確，否則將無法成功載入。
- 使用 `lsmod` 命令來檢查已載入的模組。
- 在載入模組之前，建議先查看模組的相依性，確保所有必要的模組都已載入。