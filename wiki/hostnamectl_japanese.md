# [Linux] Bash hostnamectl の使い方: ホスト名の管理

## Overview
`hostnamectl` コマンドは、システムのホスト名や関連する設定を管理するためのツールです。このコマンドを使用すると、ホスト名の表示、変更、さらにはオペレーティングシステムのバージョン情報を確認することができます。

## Usage
基本的な構文は次のとおりです。

```bash
hostnamectl [options] [arguments]
```

## Common Options
- `set-hostname`: 新しいホスト名を設定します。
- `status`: 現在のホスト名やその他の情報を表示します。
- `set-icon-name`: アイコン名を設定します。
- `set-chassis`: チャシスのタイプを設定します（例：desktop, laptop, serverなど）。

## Common Examples

### ホスト名の表示
現在のホスト名を確認するには、次のコマンドを使用します。

```bash
hostnamectl status
```

### ホスト名の変更
ホスト名を「my-new-hostname」に変更するには、次のコマンドを実行します。

```bash
sudo hostnamectl set-hostname my-new-hostname
```

### アイコン名の設定
アイコン名を「computer」に設定するには、以下のコマンドを使用します。

```bash
sudo hostnamectl set-icon-name computer
```

### チャシスの設定
チャシスのタイプを「laptop」に設定するには、次のコマンドを実行します。

```bash
sudo hostnamectl set-chassis laptop
```

## Tips
- ホスト名を変更した後は、システムを再起動する必要がない場合が多いですが、変更が反映されない場合は再起動を検討してください。
- ホスト名にはスペースや特殊文字を使用しないようにしましょう。一般的には、英数字とハイフンを使用することが推奨されます。
- `hostnamectl` コマンドは、root権限が必要な場合がありますので、必要に応じて `sudo` を使用してください。