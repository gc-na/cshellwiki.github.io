# [Linux] Bash nice 使用方法: 調整進程優先權

## Overview
`nice` 命令用於在 Unix 和 Linux 系統中調整進程的優先權。透過這個命令，使用者可以設定程式運行時的優先級，從而影響系統資源的分配。

## Usage
基本語法如下：
```
nice [options] [command]
```

## Common Options
- `-n, --adjustment=N`: 設定優先權的調整值，範圍從 -20（最高優先權）到 19（最低優先權）。
- `-h, --help`: 顯示幫助信息。
- `--version`: 顯示版本信息。

## Common Examples
1. **以默認優先權運行命令**：
   ```bash
   nice myscript.sh
   ```

2. **以較低優先權運行命令**：
   ```bash
   nice -n 10 myscript.sh
   ```

3. **以較高優先權運行命令**：
   ```bash
   nice -n -5 myscript.sh
   ```

4. **查看當前進程的優先權**：
   ```bash
   ps -o pid,ni,cmd
   ```

## Tips
- 使用 `nice` 時，請注意不要將優先權設置得過高，以免影響系統的整體性能。
- 可以結合 `renice` 命令來動態調整正在運行的進程的優先權。
- 在需要長時間運行的任務中，適當降低優先權可以讓系統保持流暢。