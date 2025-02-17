# [Linux] Bash gzip 使用法: ファイルを圧縮する

## Overview
`gzip` コマンドは、ファイルを圧縮するためのツールです。主に、テキストファイルやデータファイルのサイズを削減するために使用され、圧縮されたファイルは `.gz` 拡張子が付与されます。

## Usage
基本的な構文は次のとおりです。

```bash
gzip [options] [arguments]
```

## Common Options
- `-d` または `--decompress`: 圧縮されたファイルを解凍します。
- `-k` または `--keep`: 元のファイルを保持したまま圧縮します。
- `-v` または `--verbose`: 圧縮の進行状況を表示します。
- `-r` または `--recursive`: ディレクトリ内のすべてのファイルを再帰的に圧縮します。

## Common Examples
- 単一ファイルを圧縮する:
    ```bash
    gzip example.txt
    ```
  
- 圧縮されたファイルを解凍する:
    ```bash
    gzip -d example.txt.gz
    ```

- 元のファイルを保持して圧縮する:
    ```bash
    gzip -k example.txt
    ```

- ディレクトリ内のすべてのファイルを圧縮する:
    ```bash
    gzip -r my_directory/
    ```

- 圧縮の進行状況を表示しながら圧縮する:
    ```bash
    gzip -v example.txt
    ```

## Tips
- 大きなファイルを圧縮する際は、`-k` オプションを使用して元のファイルを保持することをお勧めします。
- 圧縮率を調整したい場合は、`gzip` の代わりに `pigz` を使用すると、マルチスレッドでの圧縮が可能です。
- 圧縮されたファイルは、`gunzip` コマンドでも解凍できます。