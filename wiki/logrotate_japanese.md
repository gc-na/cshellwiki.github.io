# [Linux] Bash logrotate の使い方: ログファイルの管理

## Overview
`logrotate` コマンドは、システムのログファイルを自動的に管理するためのツールです。ログファイルのサイズを制御し、古いログを圧縮または削除することで、ディスクスペースを効率的に使用します。

## Usage
基本的な構文は次の通りです。

```bash
logrotate [options] [arguments]
```

## Common Options
- `-f` : 強制的にログローテーションを実行します。
- `-s` : 状態ファイルのパスを指定します。
- `-v` : 詳細な出力を表示します。
- `-d` : 実行をシミュレーションし、実際には変更を加えません。

## Common Examples

### 1. デフォルト設定でのログローテーション
```bash
logrotate /etc/logrotate.conf
```

### 2. 強制的にログローテーションを実行
```bash
logrotate -f /etc/logrotate.conf
```

### 3. 詳細な出力を表示
```bash
logrotate -v /etc/logrotate.conf
```

### 4. シミュレーションモードでの実行
```bash
logrotate -d /etc/logrotate.conf
```

## Tips
- 定期的にログローテーションを行うために、cronジョブを設定することをお勧めします。
- 設定ファイルを編集する際は、バックアップを取ってから変更を加えると安心です。
- ログファイルのサイズや保持期間を適切に設定し、ディスクスペースを効率的に管理しましょう。