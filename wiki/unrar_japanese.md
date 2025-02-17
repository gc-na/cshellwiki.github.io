# [日本語] Bash unrar 使用法: RARファイルを解凍するコマンド

## Overview
`unrar` コマンドは、RAR形式の圧縮ファイルを解凍するためのツールです。これにより、RARファイル内のデータを簡単に取り出すことができます。

## Usage
基本的な構文は以下の通りです。

```
unrar [options] [arguments]
```

## Common Options
- `e` : 指定したRARファイルを解凍し、ファイルを現在のディレクトリに展開します。
- `x` : 指定したRARファイルを解凍し、元のディレクトリ構造を保持します。
- `l` : RARファイル内のファイルリストを表示します。
- `v` : 解凍したファイルの詳細情報を表示します。

## Common Examples
以下は、`unrar` コマンドの一般的な使用例です。

### RARファイルを現在のディレクトリに解凍する
```bash
unrar e archive.rar
```

### RARファイルを元のディレクトリ構造で解凍する
```bash
unrar x archive.rar
```

### RARファイル内のファイルリストを表示する
```bash
unrar l archive.rar
```

### 解凍時に詳細情報を表示する
```bash
unrar v archive.rar
```

## Tips
- 解凍先のディレクトリを指定したい場合は、`e` または `x` オプションの後にディレクトリパスを追加できます。
- RARファイルがパスワードで保護されている場合、解凍時にパスワードを入力する必要があります。
- `unrar` コマンドは、LinuxやmacOSなどのUnix系OSで広く使用されていますが、Windowsでも利用可能です。