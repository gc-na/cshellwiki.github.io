# [Linux] Bash rev コマンド: 文字列を逆にする

## Overview
`rev` コマンドは、各行の文字列を逆にするためのシンプルなツールです。このコマンドは、テキストファイルや標準入力から受け取ったデータの各行を反転させて出力します。

## Usage
基本的な構文は以下の通りです。

```bash
rev [options] [arguments]
```

## Common Options
- `-o, --output=FILE` : 出力を指定したファイルに書き込む。
- `-h, --help` : ヘルプメッセージを表示する。
- `-V, --version` : バージョン情報を表示する。

## Common Examples
以下に、`rev` コマンドの一般的な使用例を示します。

### 例1: 標準入力からの逆転
```bash
echo "Hello World" | rev
```
出力:
```
dlroW olleH
```

### 例2: ファイルの内容を逆転
ファイル `example.txt` の内容を逆転させる場合:
```bash
rev example.txt
```

### 例3: 出力を新しいファイルに保存
ファイル `output.txt` に逆転した内容を保存する場合:
```bash
rev example.txt -o output.txt
```

## Tips
- `rev` コマンドは、パイプを使って他のコマンドと組み合わせることで、より強力に活用できます。
- 大きなファイルを扱う際は、出力をファイルにリダイレクトすることで、結果を簡単に保存できます。
- スクリプト内で使用する場合、エラーハンドリングを考慮することをお勧めします。