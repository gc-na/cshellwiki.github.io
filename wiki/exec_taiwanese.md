# [Linux] Bash exec 用法: 執行命令並替換當前進程

## Overview
`exec` 命令用於在當前的 shell 環境中執行指定的命令，並用該命令替換當前的進程。這意味著當命令執行完成後，原本的 shell 將不再存在，而是被新的命令所取代。

## Usage
基本語法如下：
```bash
exec [options] [arguments]
```

## Common Options
- `-a` : 指定執行的命令名稱。
- `-l` : 使執行的命令成為 login shell。
- `-c` : 指定命令的環境變數。

## Common Examples
以下是一些常見的 `exec` 使用範例：

1. **替換當前 shell 為新的命令**
   ```bash
   exec /bin/bash
   ```
   這將用新的 bash shell 替換當前的 shell。

2. **執行一個命令並關閉當前 shell**
   ```bash
   exec ls -l
   ```
   這將列出當前目錄的文件，並在執行後關閉當前 shell。

3. **使用 `-a` 選項指定命令名稱**
   ```bash
   exec -a my_custom_name /bin/bash
   ```
   這將用新的 bash shell 替換當前的 shell，並將其命名為 `my_custom_name`。

## Tips
- 使用 `exec` 時要小心，因為一旦執行，原本的 shell 將無法恢復。
- 在腳本中使用 `exec` 可以有效地管理資源，特別是在需要替換進程的情況下。
- 如果需要保留原本的 shell，考慮使用其他命令如 `bash` 或 `sh` 來啟動新的 shell。