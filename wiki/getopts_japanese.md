# [Linux] Bash getopts 使用法: コマンドラインオプションの解析

## Overview
`getopts` コマンドは、シェルスクリプト内でコマンドラインオプションを解析するためのツールです。これにより、スクリプトに渡されたオプションを簡単に処理し、ユーザーからの入力を柔軟に受け取ることができます。

## Usage
基本的な構文は以下の通りです。

```bash
getopts optstring variable
```

- `optstring` は、受け取るオプションを指定する文字列です。
- `variable` は、オプションの値を格納するための変数です。

## Common Options
- `-a`: オプション `a` を指定します。
- `-b`: オプション `b` を指定します。
- `-c`: オプション `c` を指定します。通常、引数を必要とします。

## Common Examples

### 例1: 基本的なオプションの解析
以下のスクリプトは、`-a` と `-b` のオプションを解析します。

```bash
#!/bin/bash

while getopts "ab" option; do
  case $option in
    a) echo "オプション -a が指定されました";;
    b) echo "オプション -b が指定されました";;
    *) echo "無効なオプション";;
  esac
done
```

### 例2: 引数を必要とするオプション
次のスクリプトは、`-c` オプションに引数を必要とします。

```bash
#!/bin/bash

while getopts "c:" option; do
  case $option in
    c) echo "オプション -c が指定され、引数は $OPTARG です";;
    *) echo "無効なオプション";;
  esac
done
```

### 例3: 複数のオプションを同時に解析
以下のスクリプトは、複数のオプションを同時に解析します。

```bash
#!/bin/bash

while getopts "abc:" option; do
  case $option in
    a) echo "オプション -a が指定されました";;
    b) echo "オプション -b が指定されました";;
    c) echo "オプション -c が指定され、引数は $OPTARG です";;
    *) echo "無効なオプション";;
  esac
done
```

## Tips
- `getopts` は、オプションの順序を気にせずに解析できるため、ユーザーにとって使いやすいインターフェースを提供します。
- 引数が必要なオプションには、`:` を付けて指定します。
- スクリプトの最後で `shift $((OPTIND -1))` を使用すると、残りの引数を処理することができます。