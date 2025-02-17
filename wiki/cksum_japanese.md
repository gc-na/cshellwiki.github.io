# [Linux] Bash cksum の使い方: ファイルのチェックサムを計算する

## Overview
`cksum` コマンドは、指定したファイルのチェックサム（CRC値）とバイト数を計算します。この情報は、ファイルの整合性を確認するために使用されます。

## Usage
基本的な構文は以下の通りです。

```bash
cksum [options] [arguments]
```

## Common Options
- `-a, --algorithm=ALGORITHM` : 使用するアルゴリズムを指定します。
- `-h, --help` : ヘルプメッセージを表示します。
- `-V, --version` : バージョン情報を表示します。

## Common Examples
以下に、`cksum` コマンドのいくつかの実用的な例を示します。

### 例1: 単一ファイルのチェックサムを計算する
```bash
cksum example.txt
```

### 例2: 複数ファイルのチェックサムを計算する
```bash
cksum file1.txt file2.txt
```

### 例3: 出力をファイルに保存する
```bash
cksum example.txt > checksum.txt
```

### 例4: アルゴリズムを指定してチェックサムを計算する
```bash
cksum -a crc32 example.txt
```

## Tips
- チェックサムを使用して、ファイルが変更されていないか確認する際に役立ちます。
- 大きなファイルの場合、計算に時間がかかることがありますので、必要なファイルのみを指定することをお勧めします。
- `cksum` の出力は、他のツールと組み合わせて使用することができ、スクリプトでの自動化に便利です。