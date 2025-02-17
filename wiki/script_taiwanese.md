# [Linux] Bash script 使用方式: 記錄終端機會話

## Overview
`script` 命令用於記錄終端機會話，將所有輸入和輸出保存到一個檔案中。這對於記錄操作過程或生成教學資料非常有用。

## Usage
基本語法如下：
```
script [選項] [檔案]
```

## Common Options
- `-a`：將輸出附加到指定的檔案，而不是覆蓋。
- `-c`：執行指定的命令並記錄其輸出。
- `-f`：即時顯示輸出，方便即時查看。
- `-q`：靜默模式，不顯示開始和結束的提示。

## Common Examples
1. 開始記錄會話並將輸出保存到 `session.log`：
   ```bash
   script session.log
   ```

2. 附加到現有的記錄檔案：
   ```bash
   script -a session.log
   ```

3. 記錄執行特定命令的輸出：
   ```bash
   script -c "ls -l" command_output.log
   ```

4. 使用即時顯示功能：
   ```bash
   script -f session.log
   ```

5. 靜默模式記錄會話：
   ```bash
   script -q session.log
   ```

## Tips
- 在記錄會話時，確保檔案名稱具有描述性，以便未來查找。
- 使用 `-f` 選項可以在長時間運行的命令中即時查看輸出。
- 定期檢查記錄檔案的大小，以避免佔用過多磁碟空間。