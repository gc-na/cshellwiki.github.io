# [Linux] Bash wget 用法: 下載檔案的工具

## Overview
`wget` 是一個非互動式的網路下載工具，能夠從網路上下載檔案。它支援 HTTP、HTTPS 和 FTP 協定，並且可以在後台運行，適合用於自動化下載任務。

## Usage
基本語法如下：
```
wget [選項] [網址]
```

## Common Options
- `-O <檔名>`: 指定下載後的檔案名稱。
- `-c`: 繼續未完成的下載。
- `-q`: 靜默模式，不顯示下載進度。
- `--limit-rate=<速率>`: 限制下載速度。
- `-r`: 進行遞迴下載。

## Common Examples
以下是一些常見的使用範例：

1. 下載單一檔案：
   ```bash
   wget https://example.com/file.zip
   ```

2. 指定檔案名稱：
   ```bash
   wget -O myfile.zip https://example.com/file.zip
   ```

3. 繼續未完成的下載：
   ```bash
   wget -c https://example.com/largefile.zip
   ```

4. 靜默下載：
   ```bash
   wget -q https://example.com/file.zip
   ```

5. 遞迴下載整個網站：
   ```bash
   wget -r https://example.com/
   ```

## Tips
- 使用 `-c` 選項可以避免重新下載已經下載的部分，節省時間和帶寬。
- 在下載大檔案時，考慮使用 `--limit-rate` 選項來控制下載速度，以免佔用過多的網路資源。
- 如果需要下載多個檔案，可以將網址寫入一個文本檔，然後使用 `-i` 選項來批量下載：
   ```bash
   wget -i urls.txt
   ```