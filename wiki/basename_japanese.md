# [日本語] C Shell (csh) basename 使用法: ファイル名の取得

## Overview
`basename` コマンドは、指定したパスからファイル名を抽出し、拡張子を取り除くために使用されます。このコマンドは、ファイルのパスを簡潔に表示したいときに便利です。

## Usage
基本的な構文は以下の通りです。

```
basename [options] [arguments]
```

## Common Options
- `-a` : 複数の引数を受け取り、各引数のベース名を表示します。
- `-s` : 指定したサフィックスを取り除いてベース名を表示します。

## Common Examples
以下に、`basename` コマンドのいくつかの実用的な例を示します。

### 例 1: 単一のファイルパスからファイル名を取得
```csh
basename /path/to/file.txt
```
出力:
```
file.txt
```

### 例 2: 拡張子を取り除いたファイル名を取得
```csh
basename /path/to/file.txt .txt
```
出力:
```
file
```

### 例 3: 複数のファイルパスからファイル名を取得
```csh
basename -a /path/to/file1.txt /path/to/file2.txt
```
出力:
```
file1.txt
file2.txt
```

## Tips
- `basename` はスクリプト内でファイル名を扱う際に非常に役立ちます。
- 複数のファイルを一度に処理する場合は、`-a` オプションを使用すると便利です。
- サフィックスを指定することで、特定のファイル拡張子を除去することができます。