# [Linux] Bash sed 使用法: テキストの変換と編集

## Overview
`sed`（ストリームエディタ）は、テキストデータを処理するための強力なツールです。主に、ファイル内のテキストを検索、置換、削除、挿入するために使用されます。

## Usage
基本的な構文は次のとおりです。

```bash
sed [options] [arguments]
```

## Common Options
- `-e`: 複数の編集コマンドを指定するために使用します。
- `-i`: ファイルを直接編集します（バックアップを作成するオプションも指定可能）。
- `-n`: 出力を抑制し、特定の行のみを表示します。
- `s`: 置換コマンドを指定します。

## Common Examples
- **テキストの置換**
  ```bash
  sed 's/old-text/new-text/' filename.txt
  ```
  このコマンドは、`filename.txt`内の最初の`old-text`を`new-text`に置き換えます。

- **ファイルを直接編集**
  ```bash
  sed -i 's/old-text/new-text/g' filename.txt
  ```
  このコマンドは、`filename.txt`内のすべての`old-text`を`new-text`に置き換え、ファイルを直接編集します。

- **特定の行を表示**
  ```bash
  sed -n '2p' filename.txt
  ```
  このコマンドは、`filename.txt`の2行目のみを表示します。

- **複数の置換を行う**
  ```bash
  sed -e 's/old-text1/new-text1/g' -e 's/old-text2/new-text2/g' filename.txt
  ```
  このコマンドは、`old-text1`と`old-text2`をそれぞれ`new-text1`と`new-text2`に置き換えます。

## Tips
- 置換を行う際は、必ずバックアップを取ることをお勧めします。`-i.bak`オプションを使用すると、元のファイルのバックアップが作成されます。
- 正規表現を活用することで、より複雑なパターンマッチングが可能になります。
- 複数のファイルを一度に処理することもできるため、スクリプトでの利用に適しています。