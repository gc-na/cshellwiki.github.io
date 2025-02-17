# [日本語] Bash docker-compose 使用法: コンテナの管理とオーケストレーション

## Overview
`docker-compose` コマンドは、複数の Docker コンテナを定義し、実行するためのツールです。YAML ファイルを使用して、アプリケーションのサービス、ネットワーク、およびボリュームを簡単に管理できます。

## Usage
基本的な構文は以下の通りです。

```bash
docker-compose [options] [arguments]
```

## Common Options
- `up`: 定義されたサービスを起動します。
- `down`: 実行中のサービスを停止し、リソースをクリーンアップします。
- `build`: サービスのイメージをビルドします。
- `logs`: サービスのログを表示します。
- `exec`: 実行中のコンテナ内でコマンドを実行します。

## Common Examples
以下にいくつかの実用的な例を示します。

### サービスの起動
```bash
docker-compose up
```

### サービスの停止
```bash
docker-compose down
```

### イメージのビルド
```bash
docker-compose build
```

### ログの表示
```bash
docker-compose logs
```

### コンテナ内でのコマンド実行
```bash
docker-compose exec <サービス名> <コマンド>
```
例:
```bash
docker-compose exec web bash
```

## Tips
- `docker-compose up -d` を使用すると、バックグラウンドでサービスを起動できます。
- `docker-compose.yml` ファイルをプロジェクトのルートディレクトリに配置することを忘れないでください。
- サービスの変更後は、`docker-compose up --build` を使用して再ビルドを行うと便利です。