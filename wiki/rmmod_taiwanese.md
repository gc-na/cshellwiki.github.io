# [Linux] Bash rmmod 用法: 卸載 Linux 核心模組

## Overview
`rmmod` 是一個用於卸載 Linux 核心模組的命令。當你需要從內核中移除不再使用的模組時，可以使用這個命令來釋放系統資源。

## Usage
基本語法如下：
```bash
rmmod [選項] [模組名稱]
```

## Common Options
- `-f`：強制卸載模組，即使模組正在使用中。
- `-n`：不執行卸載，只顯示將要執行的操作。
- `--help`：顯示幫助信息。
- `--version`：顯示版本信息。

## Common Examples
以下是一些常見的使用範例：

1. 卸載一個模組：
   ```bash
   rmmod my_module
   ```

2. 強制卸載一個正在使用的模組：
   ```bash
   rmmod -f my_module
   ```

3. 顯示將要執行的操作，而不實際執行：
   ```bash
   rmmod -n my_module
   ```

4. 查看幫助信息：
   ```bash
   rmmod --help
   ```

## Tips
- 在卸載模組之前，確保該模組不再被任何進程使用，以避免系統不穩定。
- 使用 `lsmod` 命令來查看當前加載的模組，幫助你確認需要卸載的模組名稱。
- 在生產環境中，使用 `-f` 參數時要特別小心，因為這可能會導致系統不穩定或崩潰。