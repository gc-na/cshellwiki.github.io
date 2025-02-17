# [Linux] Bash psql 使用法: PostgreSQLデータベースに接続する

## Overview
`psql`コマンドは、PostgreSQLデータベースに対してインタラクティブにクエリを実行したり、データベースの管理を行ったりするためのコマンドラインツールです。このツールを使用することで、SQLコマンドを直接入力し、データベースと対話できます。

## Usage
基本的な構文は以下の通りです。

```bash
psql [options] [arguments]
```

## Common Options
- `-h` : データベースサーバーのホスト名を指定します。
- `-p` : データベースサーバーのポート番号を指定します。
- `-U` : データベースユーザー名を指定します。
- `-d` : 接続するデータベース名を指定します。
- `-W` : パスワードの入力を促します。

## Common Examples
以下は、`psql`コマンドの一般的な使用例です。

### データベースに接続する
```bash
psql -h localhost -U username -d database_name
```

### SQLファイルを実行する
```bash
psql -U username -d database_name -f script.sql
```

### データベースの一覧を表示する
```bash
psql -U username -d database_name -c "\l"
```

### テーブルの内容を表示する
```bash
psql -U username -d database_name -c "SELECT * FROM table_name;"
```

## Tips
- `\?` コマンドを入力すると、`psql`のヘルプが表示され、使用可能なコマンドを確認できます。
- `\q` コマンドで`psql`セッションを終了できます。
- SQLクエリを実行する際は、セミコロン（`;`）を忘れずに付けてください。