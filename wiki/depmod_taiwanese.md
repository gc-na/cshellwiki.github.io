# [Linux] Bash depmod 使用法: 管理內核模組依賴

## Overview
`depmod` 是一個用於生成內核模組依賴關係的工具。它會分析系統中的模組，並創建一個包含模組依賴關係的文件，通常是 `/lib/modules/$(uname -r)/modules.dep`。這對於確保內核能正確加載所需的模組非常重要。

## Usage
基本語法如下：
```
depmod [options] [arguments]
```

## Common Options
- `-a`：自動生成依賴關係，並更新所有模組。
- `-n`：僅顯示模組依賴關係，而不寫入任何文件。
- `-F <file>`：指定要使用的內核映像文件。
- `-b <directory>`：指定模組的基礎目錄。

## Common Examples
以下是一些常見的使用範例：

1. 自動生成並更新所有模組的依賴關係：
   ```bash
   depmod -a
   ```

2. 僅顯示當前模組的依賴關係，而不進行任何寫入操作：
   ```bash
   depmod -n
   ```

3. 使用特定的內核映像文件生成依賴關係：
   ```bash
   depmod -F /boot/vmlinuz-5.10.0-8-amd64
   ```

4. 指定模組的基礎目錄：
   ```bash
   depmod -b /path/to/modules
   ```

## Tips
- 在安裝新模組後，記得運行 `depmod -a` 來更新依賴關係。
- 使用 `depmod -n` 可以幫助你檢查依賴關係而不影響系統文件。
- 定期檢查模組依賴關係可以避免因缺少依賴而導致的系統問題。