# [Linux] Bash yum の使い方: パッケージ管理ツール

## Overview
`yum`（Yellowdog Updater, Modified）は、Red Hat系のLinuxディストリビューションで使用されるパッケージ管理ツールです。ソフトウェアパッケージのインストール、更新、削除を簡単に行うことができます。

## Usage
基本的な構文は以下の通りです。

```bash
yum [options] [arguments]
```

## Common Options
- `install`: 指定したパッケージをインストールします。
- `remove`: 指定したパッケージを削除します。
- `update`: インストールされているパッケージを更新します。
- `list`: 利用可能なパッケージやインストール済みのパッケージを表示します。
- `search`: 指定したキーワードに基づいてパッケージを検索します。

## Common Examples
以下は、`yum`コマンドの一般的な使用例です。

### パッケージのインストール
```bash
yum install httpd
```
このコマンドはApache HTTPサーバーをインストールします。

### パッケージの削除
```bash
yum remove httpd
```
このコマンドはApache HTTPサーバーを削除します。

### パッケージの更新
```bash
yum update
```
このコマンドはすべてのインストール済みパッケージを最新のバージョンに更新します。

### 利用可能なパッケージのリスト表示
```bash
yum list available
```
このコマンドはインストール可能なパッケージのリストを表示します。

### パッケージの検索
```bash
yum search nginx
```
このコマンドは「nginx」というキーワードを含むパッケージを検索します。

## Tips
- 定期的に`yum update`を実行して、システムを最新の状態に保ちましょう。
- `yum clean all`を使用してキャッシュをクリアし、ディスクスペースを節約できます。
- パッケージの依存関係を自動的に解決するため、`yum`は非常に便利です。依存関係の問題を気にせずにパッケージをインストールできます。