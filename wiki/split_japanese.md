# [Linux] Bash split 使用法: ファイルを分割する

## Overview
`split` コマンドは、大きなファイルを指定したサイズや行数に基づいて小さなファイルに分割するためのツールです。これにより、大きなデータセットを扱いやすくすることができます。

## Usage
基本的な構文は次のとおりです。

```
split [options] [arguments]
```

## Common Options
- `-l NUM` : 指定した行数ごとにファイルを分割します。
- `-b SIZE` : 指定したバイト数ごとにファイルを分割します。
- `-d` : 出力ファイル名に数字を使用します。
- `--additional-suffix=SUFFIX` : 出力ファイルに追加のサフィックスを付けます。

## Common Examples
以下は、`split` コマンドのいくつかの実用的な例です。

### 行数で分割
ファイルを100行ごとに分割する場合：
```bash
split -l 100 largefile.txt
```

### バイト数で分割
ファイルを1MBごとに分割する場合：
```bash
split -b 1M largefile.txt
```

### 数字を使ったファイル名で分割
ファイルを100行ごとに分割し、出力ファイル名に数字を使用する場合：
```bash
split -l 100 -d largefile.txt output_prefix_
```

### 追加のサフィックスを付けて分割
ファイルを1KBごとに分割し、出力ファイルに「.part」を追加する場合：
```bash
split -b 1K --additional-suffix=.part largefile.txt
```

## Tips
- 分割したファイルを再結合するには、`cat` コマンドを使用して結合できます。
- 大きなファイルを分割する際は、適切なサイズを選ぶことで、後の処理が容易になります。
- `split` コマンドを使う際は、出力ファイルの命名規則を考慮して、管理しやすいようにしましょう。