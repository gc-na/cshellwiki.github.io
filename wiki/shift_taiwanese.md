# [Linux] Bash shift 使用法: 參數移位

## Overview
`shift` 命令用於在 Bash 腳本中移動位置參數。當你執行 `shift` 時，所有的位置參數都會向左移動，這樣 `$1` 會變成原本的 `$2`，`$2` 會變成 `$3`，依此類推。這對於處理命令行參數非常有用。

## Usage
基本語法如下：

```bash
shift [n]
```

其中 `n` 是可選的，表示要移動的位數。預設為 1。

## Common Options
- `n`: 指定要移位的參數數量，預設為 1。

## Common Examples

### 基本用法
假設你有一個腳本接受多個參數，你可以這樣使用 `shift`：

```bash
#!/bin/bash
echo "第一個參數: $1"
shift
echo "第二個參數: $1"
```
執行腳本時，如果傳入參數 `apple banana cherry`，輸出將會是：
```
第一個參數: apple
第二個參數: banana
```

### 移位多個參數
你也可以同時移位多個參數：

```bash
#!/bin/bash
echo "第一個參數: $1"
shift 2
echo "第三個參數: $1"
```
如果傳入 `apple banana cherry`, 輸出將會是：
```
第一個參數: apple
第三個參數: cherry
```

### 與循環結合
`shift` 常與循環結合使用，以處理所有參數：

```bash
#!/bin/bash
while [ "$#" -gt 0 ]; do
    echo "處理參數: $1"
    shift
done
```
這段程式碼會逐一輸出所有傳入的參數。

## Tips
- 在使用 `shift` 時，確保你知道當前的參數數量，避免移位過多導致 `$1` 變成空。
- 可以結合 `getopts` 使用，讓參數處理更靈活。
- 使用 `shift` 時，保持代碼簡潔，避免過度嵌套的條件語句。