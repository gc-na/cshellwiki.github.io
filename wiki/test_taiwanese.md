# [Linux] Bash test 使用法: 檢查條件

## Overview
`test` 命令用於評估條件表達式，並根據結果返回真或假。這個命令在腳本中非常有用，可以用來進行檔案檢查、字串比較和數字比較等操作。

## Usage
基本語法如下：
```bash
test [options] [arguments]
```

## Common Options
- `-e FILE`：檢查檔案是否存在。
- `-d FILE`：檢查檔案是否為目錄。
- `-f FILE`：檢查檔案是否為普通檔案。
- `-z STRING`：檢查字串是否為空。
- `-n STRING`：檢查字串是否非空。
- `STRING1 = STRING2`：比較兩個字串是否相等。
- `NUM1 -eq NUM2`：檢查兩個數字是否相等。

## Common Examples
以下是一些常見的使用範例：

1. 檢查檔案是否存在：
   ```bash
   test -e myfile.txt && echo "檔案存在"
   ```

2. 檢查目錄是否存在：
   ```bash
   test -d /home/user/mydir && echo "目錄存在"
   ```

3. 檢查字串是否為空：
   ```bash
   mystring=""
   test -z "$mystring" && echo "字串是空的"
   ```

4. 比較兩個字串：
   ```bash
   test "hello" = "hello" && echo "字串相等"
   ```

5. 數字比較：
   ```bash
   num1=5
   num2=10
   test $num1 -lt $num2 && echo "$num1 小於 $num2"
   ```

## Tips
- 使用 `[` 和 `]` 來替代 `test`，例如 `[` 可以用來簡化語法：`[ -e myfile.txt ] && echo "檔案存在"`。
- 確保在字串比較時使用雙引號，以避免空格或特殊字元造成的錯誤。
- 在腳本中使用 `if` 語句結合 `test` 來提高可讀性，例如：
  ```bash
  if test -f myfile.txt; then
      echo "檔案存在"
  fi
  ```