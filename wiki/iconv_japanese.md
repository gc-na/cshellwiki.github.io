# [日本語] Bash iconv 使用法: 文字エンコーディングの変換

## Overview
`iconv` コマンドは、ファイルや標準入力の文字エンコーディングを変換するためのツールです。異なるエンコーディング間でテキストを変換することで、データの互換性を保つことができます。

## Usage
基本的な構文は以下の通りです。

```bash
iconv [options] [arguments]
```

## Common Options
- `-f` : 入力ファイルのエンコーディングを指定します。
- `-t` : 出力ファイルのエンコーディングを指定します。
- `-o` : 出力ファイルを指定します。指定しない場合は標準出力に出力されます。
- `-c` : 無効な文字をスキップします。

## Common Examples
以下にいくつかの実用的な例を示します。

### 例1: UTF-8からISO-8859-1への変換
```bash
iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
```

### 例2: Shift_JISからUTF-8への変換
```bash
iconv -f SHIFT_JIS -t UTF-8 input_sjis.txt -o output_utf8.txt
```

### 例3: 標準入力から変換
```bash
echo "こんにちは" | iconv -f UTF-8 -t EUC-JP
```

### 例4: 無効な文字をスキップして変換
```bash
iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
```

## Tips
- 変換するエンコーディングを正確に指定することで、データの損失を防ぐことができます。
- 大きなファイルを扱う場合は、出力ファイルを指定しておくと便利です。
- `iconv` のサポートするエンコーディングのリストは、`iconv -l` コマンドで確認できます。