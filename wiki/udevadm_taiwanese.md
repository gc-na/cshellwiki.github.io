# [Linux] Bash udevadm 使用說明: 管理和查詢設備

## Overview
`udevadm` 是一個用於管理和查詢 Linux 系統中設備的命令行工具。它與 udev 系統緊密集成，能夠幫助用戶監控和控制設備的行為。

## Usage
基本語法如下：
```
udevadm [options] [arguments]
```

## Common Options
- `info`：顯示設備的詳細信息。
- `trigger`：觸發 udev 事件，通常用於重新加載設備。
- `settle`：等待所有設備事件處理完成。
- `control`：控制 udev 的運行狀態，例如啟動或停止。

## Common Examples
1. **查詢設備信息**
   ```bash
   udevadm info --query=all --name=/dev/sda
   ```
   這個命令會顯示 `/dev/sda` 設備的所有詳細信息。

2. **觸發設備事件**
   ```bash
   udevadm trigger
   ```
   此命令會重新觸發所有設備的 udev 事件，通常用於在設備更改後更新系統。

3. **等待所有事件完成**
   ```bash
   udevadm settle
   ```
   使用這個命令可以確保所有的設備事件都已經處理完畢。

4. **控制 udev 服務**
   ```bash
   udevadm control --reload-rules
   ```
   這個命令會重新加載 udev 規則，通常在修改規則後使用。

## Tips
- 在進行設備管理操作之前，建議先使用 `udevadm info` 確認設備的詳細信息。
- 使用 `udevadm trigger` 時要小心，因為它會影響所有設備，可能會導致系統不穩定。
- 定期檢查和更新 udev 規則，以確保設備能夠正確識別和管理。