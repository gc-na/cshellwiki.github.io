# [Linux] C Shell (csh) update-rc.d 使用法: サービスの自動起動設定

## 概要
`update-rc.d` コマンドは、Debian系のLinuxディストリビューションでサービスの自動起動設定を管理するために使用されます。このコマンドを使うことで、システムの起動時に特定のサービスを自動的に開始したり、停止したりすることができます。

## 使用法
基本的な構文は以下の通りです。

```
update-rc.d [options] [arguments]
```

## 一般的なオプション
- `defaults` : デフォルトの起動レベルでサービスを追加します。
- `remove` : サービスを自動起動リストから削除します。
- `disable` : サービスを無効にします。
- `enable` : サービスを有効にします。

## 一般的な例
以下は `update-rc.d` コマンドの実用的な例です。

### サービスの追加
デフォルトの起動レベルでサービスを追加する場合：
```bash
sudo update-rc.d myservice defaults
```

### サービスの削除
自動起動リストからサービスを削除する場合：
```bash
sudo update-rc.d myservice remove
```

### サービスの無効化
サービスを無効にする場合：
```bash
sudo update-rc.d myservice disable
```

### サービスの有効化
サービスを再度有効にする場合：
```bash
sudo update-rc.d myservice enable
```

## ヒント
- サービスを追加する前に、必ずサービスのスクリプトが `/etc/init.d/` に存在することを確認してください。
- サービスの状態を確認するために、`service` コマンドや `systemctl` コマンドを併用すると便利です。
- 自動起動の設定を変更する際は、システムの再起動後に動作を確認することをお勧めします。