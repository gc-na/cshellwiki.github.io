# [Linux] Bash sqlite3 使用法: SQLiteデータベースを操作する

## Overview
`sqlite3` コマンドは、SQLiteデータベースを操作するためのコマンドラインインターフェースです。このコマンドを使用することで、データベースの作成、クエリの実行、データの挿入や更新、削除などが可能になります。

## Usage
基本的な構文は以下の通りです。

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help` : ヘルプメッセージを表示します。
- `-version` : SQLiteのバージョン情報を表示します。
- `-init <file>` : 指定したSQLファイルを初期化時に実行します。
- `-batch` : バッチモードで実行し、対話的なプロンプトを表示しません。

## Common Examples

### データベースの作成
新しいSQLiteデータベースを作成するには、以下のコマンドを使用します。

```bash
sqlite3 mydatabase.db
```

### テーブルの作成
データベース内にテーブルを作成するには、次のようにします。

```bash
sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT, age INTEGER);"
```

### データの挿入
テーブルにデータを挿入するには、以下のコマンドを使用します。

```bash
sqlite3 mydatabase.db "INSERT INTO users (name, age) VALUES ('Alice', 30);"
```

### データのクエリ
テーブルからデータを取得するには、次のようにします。

```bash
sqlite3 mydatabase.db "SELECT * FROM users;"
```

### データの削除
特定のデータを削除するには、以下のコマンドを使用します。

```bash
sqlite3 mydatabase.db "DELETE FROM users WHERE name='Alice';"
```

## Tips
- データベースを操作する前に、必ずバックアップを取ることをお勧めします。
- SQLクエリをファイルに保存し、`sqlite3` コマンドでそのファイルを実行することで、複雑な操作を簡単に行えます。
- データベースのサイズが大きくなる場合は、インデックスを作成してクエリのパフォーマンスを向上させることができます。