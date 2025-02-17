# [Linux] Bash ln 使用方法: 創建檔案的連結

## Overview
`ln` 命令用於在 Linux 系統中創建檔案的連結。它可以創建硬連結或符號連結，讓使用者能夠在檔案系統中以不同的方式訪問同一個檔案。

## Usage
基本語法如下：
```bash
ln [options] [arguments]
```

## Common Options
- `-s`: 創建符號連結（symlink），而不是硬連結。
- `-f`: 強制創建連結，若目標檔案已存在則覆蓋。
- `-n`: 在創建連結時不跟隨已存在的連結。
- `-v`: 顯示詳細的執行過程。

## Common Examples
1. 創建硬連結：
   ```bash
   ln original.txt link_to_original.txt
   ```

2. 創建符號連結：
   ```bash
   ln -s original.txt symlink_to_original.txt
   ```

3. 強制創建連結，覆蓋已存在的檔案：
   ```bash
   ln -f original.txt link_to_original.txt
   ```

4. 創建符號連結並顯示詳細信息：
   ```bash
   ln -sv original.txt symlink_to_original.txt
   ```

## Tips
- 使用符號連結時，請注意原始檔案的路徑。如果原始檔案被移動或刪除，符號連結將失效。
- 硬連結無法跨不同的檔案系統創建，這是它與符號連結的主要區別之一。
- 在創建連結時，確保您有足夠的權限來訪問原始檔案和目標位置。