# [台灣] Bash date 使用法: 顯示和格式化日期與時間

## Overview
`date` 命令用於顯示當前的日期和時間，並可以根據使用者的需求進行格式化。這個命令在腳本中非常有用，特別是當需要記錄時間戳或生成日期相關的文件名稱時。

## Usage
基本語法如下：
```
date [options] [arguments]
```

## Common Options
- `+FORMAT`：自定義輸出格式。
- `-u`：以協調世界時（UTC）顯示日期和時間。
- `-d STRING`：顯示指定日期的時間。
- `-R`：以 RFC 2822 格式顯示日期和時間。

## Common Examples
1. 顯示當前日期和時間：
   ```bash
   date
   ```

2. 以自定義格式顯示日期：
   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

3. 顯示 UTC 時間：
   ```bash
   date -u
   ```

4. 顯示指定日期的時間：
   ```bash
   date -d "2023-10-01"
   ```

5. 以 RFC 2822 格式顯示日期：
   ```bash
   date -R
   ```

## Tips
- 使用 `date +%F` 可以快速獲得 ISO 8601 格式的日期（YYYY-MM-DD）。
- 結合 `date` 和其他命令，例如用於命名文件時，可以這樣使用：
  ```bash
  touch "backup_$(date +%Y-%m-%d).tar.gz"
  ```
- 若要獲得當前時間戳，可以使用 `date +%s`。