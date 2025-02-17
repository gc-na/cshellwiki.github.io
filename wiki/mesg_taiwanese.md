# [Linux] Bash mesg 用法: 控制訊息接收

## Overview
`mesg` 命令用來控制使用者是否可以接收來自其他使用者的訊息。這在多使用者環境中非常有用，讓使用者能夠選擇是否允許其他人發送訊息給他們。

## Usage
基本語法如下：
```
mesg [options] [arguments]
```

## Common Options
- `y`：允許其他使用者發送訊息。
- `n`：禁止其他使用者發送訊息。
- `--help`：顯示幫助訊息。

## Common Examples
1. 允許接收訊息：
   ```bash
   mesg y
   ```

2. 禁止接收訊息：
   ```bash
   mesg n
   ```

3. 查看當前的訊息接收狀態：
   ```bash
   mesg
   ```

## Tips
- 在共享環境中，根據需要調整訊息接收設定，以避免不必要的干擾。
- 使用 `mesg` 命令時，請注意其他使用者的需求，適時調整設定以保持良好的溝通。