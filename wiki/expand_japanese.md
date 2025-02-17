# [Linux] Bash expand 使用法: テキストのタブをスペースに変換する

## Overview
`expand` コマンドは、テキストファイル内のタブ文字をスペースに変換するためのツールです。これにより、異なる環境での表示を統一し、フォーマットを整えることができます。

## Usage
基本的な構文は以下の通りです。

```
expand [options] [arguments]
```

## Common Options
- `-t, --tabs=N` : タブの幅を N スペースに設定します。
- `-i, --initial` : 行の先頭にあるタブのみを変換します。
- `-n, --no-tabs` : タブを変換せず、そのまま出力します。

## Common Examples
以下は、`expand` コマンドのいくつかの実用的な例です。

### 例1: 基本的な使用法
タブをスペースに変換する基本的なコマンドです。
```bash
expand input.txt > output.txt
```

### 例2: タブの幅を指定する
タブの幅を 4 スペースに設定して変換します。
```bash
expand -t 4 input.txt > output.txt
```

### 例3: 行の先頭のタブのみを変換
行の先頭にあるタブだけをスペースに変換します。
```bash
expand -i input.txt > output.txt
```

### 例4: タブを変換せずに出力
タブをそのまま出力する場合に使用します。
```bash
expand -n input.txt > output.txt
```

## Tips
- `expand` を使用する際は、出力ファイルを指定することで元のファイルを保持できます。
- スペースの幅を変更したい場合は、`-t` オプションを活用してください。
- スクリプト内での使用時には、標準入力からの読み込みも可能です。