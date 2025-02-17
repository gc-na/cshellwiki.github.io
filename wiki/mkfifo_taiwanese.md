# [Linux] Bash mkfifo 使用方法: 創建命名管道

## Overview
`mkfifo` 命令用於創建命名管道（FIFO），這是一種特殊的文件類型，允許進程之間進行通信。命名管道可以讓一個進程將數據寫入管道，而另一個進程則可以從中讀取數據。

## Usage
基本語法如下：
```bash
mkfifo [options] [arguments]
```

## Common Options
- `-m, --mode=MODE`：設置新創建的 FIFO 文件的權限模式。
- `--help`：顯示幫助信息並退出。
- `--version`：顯示版本信息並退出。

## Common Examples
以下是一些常見的使用範例：

1. 創建一個名為 `myfifo` 的命名管道：
   ```bash
   mkfifo myfifo
   ```

2. 創建一個命名管道並設置特定的權限模式：
   ```bash
   mkfifo -m 644 myfifo
   ```

3. 使用命名管道進行進程間通信：
   - 在一個終端中，啟動一個讀取進程：
     ```bash
     cat < myfifo
     ```
   - 在另一個終端中，寫入數據到命名管道：
     ```bash
     echo "Hello, World!" > myfifo
     ```

## Tips
- 確保在使用命名管道之前，至少有一個進程在等待讀取數據，否則寫入操作將會阻塞。
- 使用 `-m` 參數來設置合適的權限，確保其他用戶能夠正確訪問 FIFO 文件。
- 可以使用 `rm` 命令刪除不再需要的命名管道文件。