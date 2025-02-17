# [Linux] Bash strace 使用法: 追蹤系統呼叫和信號

## Overview
`strace` 是一個強大的工具，用於追蹤程序的系統呼叫和接收到的信號。它可以幫助開發者和系統管理員診斷問題，了解程序的行為，並進行性能分析。

## Usage
基本語法如下：
```bash
strace [options] [arguments]
```

## Common Options
- `-c`：統計系統呼叫的次數和時間。
- `-e trace=<set>`：指定要追蹤的系統呼叫類型。
- `-p <pid>`：附加到已存在的進程，根據進程ID進行追蹤。
- `-o <file>`：將輸出寫入指定的文件，而不是標準輸出。
- `-f`：追蹤由 fork() 產生的子進程。

## Common Examples
1. **追蹤一個命令的系統呼叫**
   ```bash
   strace ls
   ```

2. **將輸出寫入文件**
   ```bash
   strace -o output.txt ls
   ```

3. **追蹤特定的系統呼叫**
   ```bash
   strace -e trace=open,close ls
   ```

4. **附加到一個正在運行的進程**
   ```bash
   strace -p 1234
   ```

5. **統計系統呼叫的使用情況**
   ```bash
   strace -c ls
   ```

## Tips
- 在使用 `strace` 時，對於大量輸出的命令，考慮將輸出重定向到文件，以便後續分析。
- 使用 `-e trace` 選項來限制追蹤的系統呼叫，這樣可以減少輸出並專注於特定的行為。
- 當追蹤長時間運行的進程時，使用 `-p` 選項可以避免重新啟動進程，節省時間。