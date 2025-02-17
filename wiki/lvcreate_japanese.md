# [Linux] Bash lvcreate の使い方: 論理ボリュームを作成する

## Overview
`lvcreate` コマンドは、Linuxの論理ボリュームマネージャー（LVM）を使用して新しい論理ボリュームを作成するためのツールです。このコマンドを使用することで、ストレージの管理が柔軟になり、必要に応じてボリュームを調整することができます。

## Usage
基本的な構文は以下の通りです。

```
lvcreate [options] [arguments]
```

## Common Options
- `-n, --name <name>`: 作成する論理ボリュームの名前を指定します。
- `-L, --size <size>`: 論理ボリュームのサイズを指定します。
- `-l, --extents <number>`: 論理ボリュームのエクステント数を指定します。
- `-Z, --zero n`: 新しい論理ボリュームをゼロで初期化するかどうかを指定します（`y` または `n`）。
- `-C, --mirrors <number>`: 論理ボリュームのミラー数を指定します。

## Common Examples
以下に、`lvcreate` コマンドのいくつかの実用的な例を示します。

### 例1: 新しい論理ボリュームを作成する
```bash
lvcreate -n my_volume -L 10G my_volume_group
```
このコマンドは、`my_volume_group` 内に `my_volume` という名前の10GBの論理ボリュームを作成します。

### 例2: サイズをエクステントで指定して論理ボリュームを作成する
```bash
lvcreate -n my_extents_volume -l 100 my_volume_group
```
このコマンドは、`my_volume_group` 内に100エクステントの論理ボリュームを作成します。

### 例3: ミラー付きの論理ボリュームを作成する
```bash
lvcreate -n my_mirrored_volume -m 1 -L 20G my_volume_group
```
このコマンドは、`my_volume_group` 内に20GBのミラー付き論理ボリュームを作成します。

## Tips
- 論理ボリュームを作成する前に、必ずボリュームグループが存在することを確認してください。
- 論理ボリュームのサイズは、物理ボリュームの空き容量を超えないように設定してください。
- 論理ボリュームの名前は、わかりやすく一貫性のあるものにすると管理が容易になります。