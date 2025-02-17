# [台灣] Bash flatpak 使用方式: 管理應用程式的工具

## Overview
`flatpak` 是一個用於管理和安裝應用程式的工具，特別是在 Linux 系統上。它允許用戶以獨立的方式安裝和運行應用程式，無需擔心依賴性問題，並提供了沙盒環境來提高安全性。

## Usage
基本語法如下：
```
flatpak [options] [arguments]
```

## Common Options
- `install`: 安裝指定的應用程式。
- `uninstall`: 卸載已安裝的應用程式。
- `update`: 更新已安裝的應用程式。
- `list`: 列出所有已安裝的應用程式。
- `run`: 運行指定的應用程式。

## Common Examples
安裝應用程式：
```bash
flatpak install flathub org.videolan.VLC
```

卸載應用程式：
```bash
flatpak uninstall org.videolan.VLC
```

更新所有應用程式：
```bash
flatpak update
```

列出所有已安裝的應用程式：
```bash
flatpak list
```

運行應用程式：
```bash
flatpak run org.videolan.VLC
```

## Tips
- 使用 `flatpak search [應用程式名稱]` 可以快速找到可安裝的應用程式。
- 定期運行 `flatpak update` 以保持應用程式的最新狀態。
- 了解應用程式的沙盒權限，使用 `flatpak info --show-permissions [應用程式名稱]` 來檢查。