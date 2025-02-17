# [台灣] Bash unzip 用法: 解壓縮檔案

## Overview
`unzip` 命令用於解壓縮 ZIP 格式的檔案。它能夠將壓縮檔中的內容提取到指定的目錄中，方便使用者訪問和管理檔案。

## Usage
基本語法如下：
```
unzip [選項] [檔案]
```

## Common Options
- `-d [目錄]`：指定解壓縮的目錄。
- `-l`：列出 ZIP 檔案中的檔案清單，但不解壓縮。
- `-o`：自動覆蓋已存在的檔案而不提示。
- `-q`：安靜模式，減少輸出信息。

## Common Examples
以下是一些常見的使用範例：

1. 解壓縮檔案到當前目錄：
   ```bash
   unzip example.zip
   ```

2. 解壓縮檔案到指定目錄：
   ```bash
   unzip example.zip -d /path/to/directory
   ```

3. 列出 ZIP 檔案中的檔案清單：
   ```bash
   unzip -l example.zip
   ```

4. 自動覆蓋已存在的檔案：
   ```bash
   unzip -o example.zip
   ```

5. 在安靜模式下解壓縮：
   ```bash
   unzip -q example.zip
   ```

## Tips
- 在解壓縮之前，使用 `unzip -l` 來查看檔案內容，確保你知道將要解壓縮的檔案。
- 若要避免覆蓋檔案，請在解壓縮時不使用 `-o` 選項，這樣系統會提示你是否覆蓋。
- 定期清理不需要的解壓縮檔案，以節省磁碟空間。