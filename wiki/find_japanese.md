# [Linux] Bash find コマンド: ファイル名を検索する

## Overview
`find` コマンドは、指定したディレクトリ内でファイルやディレクトリを検索するための強力なツールです。条件を指定することで、特定のファイルを効率的に見つけることができます。

## Usage
基本的な構文は以下の通りです。

```bash
find [options] [arguments]
```

## Common Options
- `-name <name>`: 指定した名前のファイルを検索します。
- `-type <type>`: ファイルの種類を指定します（例: `f` は通常のファイル、`d` はディレクトリ）。
- `-size <size>`: 指定したサイズのファイルを検索します。
- `-mtime <n>`: 最終更新日が n 日前のファイルを検索します。
- `-exec <command> {} \;`: 検索結果に対して指定したコマンドを実行します。

## Common Examples
以下は、`find` コマンドの実用的な例です。

### 例1: 特定の名前のファイルを検索
```bash
find /path/to/directory -name "example.txt"
```

### 例2: ディレクトリ内のすべてのディレクトリを検索
```bash
find /path/to/directory -type d
```

### 例3: 1MB以上のファイルを検索
```bash
find /path/to/directory -size +1M
```

### 例4: 最終更新日が7日前のファイルを検索
```bash
find /path/to/directory -mtime -7
```

### 例5: 検索結果を削除する
```bash
find /path/to/directory -name "temp*" -exec rm {} \;
```

## Tips
- 検索を行う際は、必要なディレクトリを指定することで、検索時間を短縮できます。
- `-print` オプションを使用すると、検索結果を標準出力に表示できます（デフォルトでは表示されます）。
- 複雑な条件を組み合わせることで、より精密な検索が可能です。