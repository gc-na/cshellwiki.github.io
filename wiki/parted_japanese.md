# [Linux] C Shell (csh) parted 使用法: パーティションを管理する

## Overview
`parted` コマンドは、ディスクのパーティションを作成、削除、サイズ変更、管理するためのツールです。このコマンドを使用することで、ディスクのパーティションテーブルを操作し、ストレージの効率を最大化できます。

## Usage
基本的な構文は以下の通りです。

```
parted [options] [arguments]
```

## Common Options
- `-l` : システム上のすべてのディスクとパーティションのリストを表示します。
- `mkpart` : 新しいパーティションを作成します。
- `rm` : 指定したパーティションを削除します。
- `resizepart` : 既存のパーティションのサイズを変更します。
- `print` : 現在のパーティションテーブルを表示します。

## Common Examples
以下に、`parted` コマンドの一般的な使用例を示します。

### 1. パーティションのリストを表示
```bash
parted -l
```

### 2. 新しいパーティションを作成
```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### 3. パーティションを削除
```bash
parted /dev/sda rm 1
```

### 4. パーティションのサイズを変更
```bash
parted /dev/sda resizepart 1 200MiB
```

### 5. 現在のパーティションテーブルを表示
```bash
parted /dev/sda print
```

## Tips
- `parted` コマンドを使用する前に、必ず重要なデータのバックアップを取ってください。
- パーティションの変更はデータ損失を引き起こす可能性があるため、慎重に操作を行いましょう。
- `parted` を実行するには、管理者権限が必要な場合があります。必要に応じて `sudo` を使用してください。