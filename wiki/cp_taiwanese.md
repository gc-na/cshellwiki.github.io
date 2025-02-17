# [Linux] Bash cp 使用法: 複製檔案和目錄

## Overview
`cp` 命令用於在 Linux 系統中複製檔案和目錄。它可以將一個或多個檔案從一個位置複製到另一個位置，並提供多種選項來控制複製的行為。

## Usage
基本語法如下：
```bash
cp [options] [source] [destination]
```

## Common Options
- `-r`：遞迴複製目錄及其內容。
- `-i`：在覆蓋檔案之前提示使用者確認。
- `-u`：僅在源檔案較新或目標檔案不存在時才複製。
- `-v`：顯示詳細的操作過程。
- `-a`：以檔案的所有屬性進行複製，等同於 `-dR --preserve=all`。

## Common Examples
- 複製單個檔案：
```bash
cp file.txt /path/to/destination/
```

- 複製多個檔案到目錄：
```bash
cp file1.txt file2.txt /path/to/destination/
```

- 遞迴複製目錄：
```bash
cp -r /path/to/source_directory /path/to/destination_directory
```

- 使用提示確認覆蓋：
```bash
cp -i file.txt /path/to/destination/
```

- 顯示詳細過程的複製：
```bash
cp -v file.txt /path/to/destination/
```

## Tips
- 在複製重要檔案時，建議使用 `-i` 選項，以避免意外覆蓋。
- 使用 `-u` 選項可以幫助您僅更新較舊的檔案，節省時間和空間。
- 當需要保留檔案屬性時，使用 `-a` 選項是最佳選擇。