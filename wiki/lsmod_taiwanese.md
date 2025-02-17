# [Linux] Bash lsmod 使用法: 列出已載入的模組

## Overview
`lsmod` 是一個用於顯示當前已載入的內核模組的命令。這個命令可以幫助用戶了解系統中哪些模組正在運行，以及它們的依賴關係。

## Usage
基本語法如下：
```bash
lsmod [options]
```

## Common Options
- `-h`, `--help`: 顯示幫助信息。
- `-v`, `--version`: 顯示版本信息。

## Common Examples
1. **列出所有已載入的模組**
   ```bash
   lsmod
   ```

2. **顯示幫助信息**
   ```bash
   lsmod --help
   ```

3. **顯示版本信息**
   ```bash
   lsmod --version
   ```

## Tips
- 使用 `lsmod` 可以快速檢查系統的模組狀態，特別是在進行故障排除時。
- 結合 `grep` 使用，可以快速查找特定的模組，例如：
  ```bash
  lsmod | grep <module_name>
  ```
- 定期檢查已載入的模組，有助於保持系統的穩定性和安全性。