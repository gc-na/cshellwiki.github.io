# [Linux] Bash split 使用方式: 將檔案分割成多個小檔案

## Overview
`split` 命令用於將一個大檔案分割成多個小檔案，方便管理和傳輸。這在處理大型檔案時特別有用，讓使用者能夠更輕鬆地處理和分享資料。

## Usage
基本語法如下：
```
split [options] [arguments]
```

## Common Options
- `-l NUM`：根據行數分割檔案，每個小檔案包含 NUM 行。
- `-b SIZE`：根據檔案大小分割檔案，每個小檔案的大小為 SIZE。
- `-d`：使用數字後綴來命名分割後的檔案。
- `--additional-suffix=SUFFIX`：為分割後的檔案添加額外的副檔名。

## Common Examples
- 根據行數分割檔案：
  ```bash
  split -l 100 largefile.txt smallfile_
  ```
  這會將 `largefile.txt` 每 100 行分割成小檔案，命名為 `smallfile_aa`, `smallfile_ab` 等。

- 根據檔案大小分割檔案：
  ```bash
  split -b 1M largefile.txt smallfile_
  ```
  這會將 `largefile.txt` 每 1MB 分割成小檔案。

- 使用數字後綴：
  ```bash
  split -d -l 50 largefile.txt smallfile_
  ```
  這會將檔案每 50 行分割，並使用數字後綴命名，例如 `smallfile_00`, `smallfile_01`。

- 添加額外副檔名：
  ```bash
  split --additional-suffix=.txt -l 10 largefile.txt smallfile_
  ```
  這會將每個小檔案命名為 `smallfile_aa.txt`, `smallfile_ab.txt` 等。

## Tips
- 在分割檔案之前，確保了解檔案的內容和結構，以避免在不適當的地方分割。
- 使用 `-d` 選項可以讓檔案命名更具可讀性，特別是在處理大量檔案時。
- 考慮使用 `cat` 命令來合併分割後的檔案，這樣可以方便地恢復原始檔案。