# [Linux] Bash dig の使い方: DNS情報を取得する

## Overview
`dig` コマンドは、DNS（ドメインネームシステム）に関する情報を取得するためのツールです。特定のドメイン名に関連するDNSレコードを照会し、詳細な情報を表示します。

## Usage
基本的な構文は以下の通りです。

```bash
dig [options] [arguments]
```

## Common Options
- `@server` : 指定したDNSサーバーを使用してクエリを実行します。
- `-t type` : 照会するDNSレコードのタイプを指定します（例: A, MX, TXTなど）。
- `+short` : 簡潔な出力を表示します。
- `+trace` : DNSクエリのトレースを行い、各ステップを表示します。

## Common Examples
以下は、`dig` コマンドの一般的な使用例です。

### 1. 基本的なAレコードの照会
```bash
dig example.com
```

### 2. 特定のDNSサーバーを指定して照会
```bash
dig @8.8.8.8 example.com
```

### 3. MXレコードの照会
```bash
dig -t MX example.com
```

### 4. 簡潔な出力を表示
```bash
dig +short example.com
```

### 5. DNSクエリのトレース
```bash
dig +trace example.com
```

## Tips
- DNS情報を確認する際は、複数のDNSサーバーを使用して結果を比較すると良いでしょう。
- `+short` オプションを使うことで、必要な情報だけを迅速に取得できます。
- `dig` コマンドは、ネットワークのトラブルシューティングにも役立ちます。