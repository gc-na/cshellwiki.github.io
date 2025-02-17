# [Linux] Bash basename の使い方: ファイル名を取得する

## Overview
`basename` コマンドは、指定したパスからファイル名を抽出するためのコマンドです。このコマンドを使用することで、フルパスから不要な部分を取り除き、シンプルなファイル名だけを取得できます。

## Usage
基本的な構文は以下の通りです。

```bash
basename [options] [arguments]
```

## Common Options
- `-a`: 複数の引数を指定した場合、すべてのファイル名を表示します。
- `-s`: 指定したサフィックスをファイル名から削除します。

## Common Examples
以下にいくつかの実用的な例を示します。

### 例1: 単一のファイル名を取得
フルパスからファイル名を取得する基本的な使い方です。

```bash
basename /home/user/documents/file.txt
```
出力:
```
file.txt
```

### 例2: 複数のファイル名を取得
`-a` オプションを使用して、複数のファイル名を取得します。

```bash
basename -a /home/user/documents/file1.txt /home/user/documents/file2.txt
```
出力:
```
file1.txt
file2.txt
```

### 例3: サフィックスを削除
`-s` オプションを使用して、ファイル名から特定のサフィックスを削除します。

```bash
basename -s .txt /home/user/documents/file.txt
```
出力:
```
file
```

## Tips
- `basename` コマンドはスクリプト内でファイル名を処理する際に非常に便利です。
- 複数のファイルを扱う場合は、`-a` オプションを活用して効率的に処理しましょう。
- サフィックスを指定する際は、正確に指定することで、不要な部分を確実に削除できます。