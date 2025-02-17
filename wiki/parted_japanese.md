# [Linux] Bash parted の使い方: パーティションの管理

## Overview
`parted` コマンドは、ディスクのパーティションを管理するためのツールです。これにより、パーティションの作成、削除、サイズ変更、フォーマットなどを行うことができます。

## Usage
基本的な構文は以下の通りです。

```bash
parted [options] [arguments]
```

## Common Options
- `-l`, `--list` : システム上のすべてのディスクとパーティションのリストを表示します。
- `mkpart` : 新しいパーティションを作成します。
- `rm` : 指定したパーティションを削除します。
- `resizepart` : 既存のパーティションのサイズを変更します。
- `print` : 現在のパーティションテーブルを表示します。

## Common Examples
以下は、`parted` コマンドの一般的な使用例です。

### 1. ディスクのリストを表示する
```bash
parted -l
```

### 2. 新しいパーティションを作成する
```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### 3. パーティションを削除する
```bash
parted /dev/sda rm 1
```

### 4. パーティションのサイズを変更する
```bash
parted /dev/sda resizepart 1 200MiB
```

### 5. 現在のパーティションテーブルを表示する
```bash
parted /dev/sda print
```

## Tips
- `parted` を使用する際は、必ず管理者権限（sudo）で実行してください。
- パーティション操作を行う前に、重要なデータのバックアップを取ることをお勧めします。
- `parted` の操作は即時に反映されるため、慎重にコマンドを入力してください。