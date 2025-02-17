# [Linux] Bash swapoff 用法: 關閉交換空間

## Overview
`swapoff` 命令用於關閉系統中的交換空間（swap space）。當系統的物理記憶體不足時，交換空間可以用來臨時存儲不活躍的數據。使用 `swapoff` 可以釋放這部分空間，讓系統更有效地使用物理記憶體。

## Usage
基本語法如下：
```
swapoff [options] [arguments]
```

## Common Options
- `-a`：關閉所有的交換空間。
- `-e`：強制關閉指定的交換空間，即使有進程在使用它。
- `-h`：顯示幫助信息。

## Common Examples
1. 關閉所有交換空間：
   ```bash
   swapoff -a
   ```

2. 關閉特定的交換檔案：
   ```bash
   swapoff /swapfile
   ```

3. 強制關閉交換空間：
   ```bash
   swapoff -e /dev/sda2
   ```

4. 查看當前的交換空間狀態（使用 `swapon` 命令）：
   ```bash
   swapon --show
   ```

## Tips
- 在關閉交換空間之前，確保系統有足夠的物理記憶體，以避免系統性能下降。
- 使用 `swapoff` 後，建議檢查系統的記憶體使用情況，確保沒有過多的進程因為缺少交換空間而受到影響。
- 如果需要重新啟用交換空間，可以使用 `swapon` 命令。