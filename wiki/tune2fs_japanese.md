# [Linux] Bash tune2fs の使い方: ファイルシステムの調整

## Overview
`tune2fs` コマンドは、Linux の ext2、ext3、ext4 ファイルシステムのパラメータを調整するために使用されます。このコマンドを使うことで、ファイルシステムの特性を変更したり、最適化したりすることができます。

## Usage
基本的な構文は以下の通りです。

```bash
tune2fs [options] [arguments]
```

## Common Options
- `-c <max-mount-count>`: 最大マウント回数を設定します。
- `-i <interval>`: 最後のチェックからの経過時間を指定します。
- `-O <feature>`: 特定のファイルシステム機能を有効にします。
- `-E <extended-options>`: 拡張オプションを指定します。
- `-L <label>`: ファイルシステムのラベルを設定します。

## Common Examples
以下に、`tune2fs` コマンドの実用的な例を示します。

### 1. 最大マウント回数の設定
```bash
sudo tune2fs -c 20 /dev/sda1
```
このコマンドは、`/dev/sda1` の最大マウント回数を 20 に設定します。

### 2. チェック間隔の設定
```bash
sudo tune2fs -i 30d /dev/sda1
```
このコマンドは、ファイルシステムのチェックを 30 日ごとに行うように設定します。

### 3. ファイルシステム機能の有効化
```bash
sudo tune2fs -O dir_index /dev/sda1
```
このコマンドは、`/dev/sda1` でディレクトリインデックス機能を有効にします。

### 4. ファイルシステムラベルの設定
```bash
sudo tune2fs -L mylabel /dev/sda1
```
このコマンドは、`/dev/sda1` のファイルシステムラベルを `mylabel` に設定します。

## Tips
- `tune2fs` を使用する前に、必ずファイルシステムをアンマウントしてください。
- 重要な変更を行う前に、データのバックアップを取ることをお勧めします。
- `tune2fs` のオプションを使用する際は、`man tune2fs` コマンドで詳細なドキュメントを確認してください。