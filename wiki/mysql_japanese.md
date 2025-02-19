# [Linux] C Shell (csh) mysql の使い方: データベースにアクセスするコマンド

## Overview
`mysql` コマンドは、MySQLデータベースにアクセスし、データベースの操作を行うためのクライアントツールです。このコマンドを使用することで、データベースのクエリを実行したり、データを管理したりすることができます。

## Usage
基本的な構文は以下の通りです。

```bash
mysql [options] [arguments]
```

## Common Options
- `-u [username]` : データベースに接続するためのユーザー名を指定します。
- `-p` : パスワードの入力を促します。
- `-h [hostname]` : 接続するデータベースサーバーのホスト名を指定します。
- `-D [database]` : 接続するデータベース名を指定します。

## Common Examples
以下は、`mysql` コマンドのいくつかの実用的な例です。

### デフォルトのデータベースに接続
```bash
mysql -u root -p
```

### 特定のデータベースに接続
```bash
mysql -u user -p -D mydatabase
```

### リモートサーバーに接続
```bash
mysql -u user -p -h 192.168.1.100
```

### SQLファイルを実行
```bash
mysql -u user -p mydatabase < script.sql
```

## Tips
- パスワードをコマンドラインに直接入力するのは避け、`-p` オプションを使用してプロンプトから入力することをお勧めします。
- 接続後は、`SHOW DATABASES;` コマンドを使って利用可能なデータベースの一覧を表示できます。
- 複雑なクエリを実行する際は、SQLファイルを作成し、`<` 演算子を使用して実行するのが便利です。