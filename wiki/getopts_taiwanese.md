# [Linux] Bash getopts 用法: 解析命令行選項

## Overview
`getopts` 是一個用於解析命令行選項的 Bash 內建命令。它可以幫助腳本從命令行中提取選項及其參數，讓使用者能夠更靈活地控制腳本的行為。

## Usage
基本語法如下：
```
getopts [options] [arguments]
```

## Common Options
- `-a`：指定選項的字母。
- `-b`：允許選項後面跟隨參數。
- `-c`：指定選項的長度。

## Common Examples
以下是一些常見的使用範例：

### 基本範例
這個範例展示如何使用 `getopts` 解析選項：
```bash
#!/bin/bash

while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "選項 A 被選擇"
      ;;
    b)
      echo "選項 B 的參數是: $OPTARG"
      ;;
    c)
      echo "選項 C 的參數是: $OPTARG"
      ;;
    *)
      echo "無效的選項"
      ;;
  esac
done
```

### 帶參數的選項
這個範例展示如何處理帶參數的選項：
```bash
#!/bin/bash

while getopts "u:p:" opt; do
  case $opt in
    u)
      echo "用戶名: $OPTARG"
      ;;
    p)
      echo "密碼: $OPTARG"
      ;;
    *)
      echo "無效的選項"
      ;;
  esac
done
```

### 多個選項
這個範例展示如何同時處理多個選項：
```bash
#!/bin/bash

while getopts "x:y:z:" opt; do
  case $opt in
    x)
      echo "選項 X 的參數是: $OPTARG"
      ;;
    y)
      echo "選項 Y 的參數是: $OPTARG"
      ;;
    z)
      echo "選項 Z 的參數是: $OPTARG"
      ;;
    *)
      echo "無效的選項"
      ;;
  esac
done
```

## Tips
- 確保選項字母是唯一的，避免混淆。
- 使用 `OPTARG` 變數來獲取選項的參數。
- 在腳本中添加錯誤處理，以便在無效選項被提供時給出提示。