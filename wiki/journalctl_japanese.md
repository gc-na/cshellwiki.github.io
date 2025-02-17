# [Linux] Bash journalctl の使い方: システムログの表示

## Overview
`journalctl` コマンドは、systemd ジャーナルからログメッセージを表示するためのツールです。これにより、システムの状態やアプリケーションの動作を監視することができます。

## Usage
基本的な構文は次の通りです。

```
journalctl [options] [arguments]
```

## Common Options
- `-b` : 現在のブートからのログを表示します。
- `-f` : 新しいログエントリをリアルタイムで追跡します。
- `--since` : 指定した日時以降のログを表示します。
- `--until` : 指定した日時までのログを表示します。
- `-u` : 特定のユニット（サービス）のログを表示します。

## Common Examples
以下は、`journalctl` コマンドのいくつかの実用的な例です。

### 1. 現在のブートからのログを表示
```bash
journalctl -b
```

### 2. リアルタイムでログを追跡
```bash
journalctl -f
```

### 3. 特定の日時以降のログを表示
```bash
journalctl --since "2023-10-01 10:00:00"
```

### 4. 特定のユニットのログを表示
```bash
journalctl -u ssh.service
```

### 5. 過去のブートのログを表示
```bash
journalctl -b -1
```

## Tips
- ログが多くなると、必要な情報を見つけるのが難しくなるため、`--grep` オプションを使って特定のキーワードでフィルタリングすると便利です。
- `-n` オプションを使うと、最新の N 行だけを表示できます。例えば、最新の 50 行を表示するには `journalctl -n 50` とします。
- 日時のフォーマットは柔軟で、`"yesterday"` や `"1 hour ago"` なども使用できます。