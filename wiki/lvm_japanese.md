# [Linux] Bash lvm 使用法: 論理ボリューム管理

## 概要
`lvm` コマンドは、Linuxの論理ボリュームマネージャー（LVM）を操作するためのツールです。これにより、ストレージデバイスの管理、論理ボリュームの作成、削除、サイズ変更などが可能になります。

## 使用法
基本的な構文は以下の通りです。

```bash
lvm [options] [arguments]
```

## 一般的なオプション
- `create`: 新しい論理ボリュームを作成します。
- `remove`: 論理ボリュームを削除します。
- `extend`: 論理ボリュームのサイズを増やします。
- `reduce`: 論理ボリュームのサイズを減らします。
- `lvdisplay`: 論理ボリュームの詳細情報を表示します。

## 一般的な例
以下に、`lvm` コマンドの実用的な例を示します。

### 論理ボリュームの作成
```bash
lvcreate -n my_volume -L 10G my_volume_group
```

### 論理ボリュームの削除
```bash
lvremove /dev/my_volume_group/my_volume
```

### 論理ボリュームのサイズを増やす
```bash
lvextend -L +5G /dev/my_volume_group/my_volume
```

### 論理ボリュームのサイズを減らす
```bash
lvreduce -L -5G /dev/my_volume_group/my_volume
```

### 論理ボリュームの詳細情報を表示
```bash
lvdisplay /dev/my_volume_group/my_volume
```

## ヒント
- 論理ボリュームのサイズを変更する前に、必ずバックアップを取ってください。
- 論理ボリュームを縮小する際は、データが失われないように、必ずファイルシステムを縮小してから行ってください。
- `lvm` コマンドを使用する際は、スーパーユーザー権限が必要です。`sudo` を使用してコマンドを実行してください。