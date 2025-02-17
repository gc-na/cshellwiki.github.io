# [Linux] Bash scp の使い方: リモートファイルの安全な転送

## 概要
`scp`（Secure Copy Protocol）は、SSH（Secure Shell）を利用してリモートホスト間でファイルを安全に転送するためのコマンドです。このコマンドは、データの暗号化を行い、セキュリティを確保しながらファイルをコピーします。

## 使用法
基本的な構文は以下の通りです。

```bash
scp [オプション] [転送元] [転送先]
```

## 一般的なオプション
- `-r`: ディレクトリを再帰的にコピーします。
- `-P`: ポート番号を指定します（大文字のP）。
- `-i`: 指定したSSH鍵を使用します。
- `-v`: 詳細な出力を表示します（デバッグ用）。

## 一般的な例
以下はいくつかの実用的な例です。

1. **ローカルからリモートへファイルをコピーする**:
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. **リモートからローカルへファイルをコピーする**:
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. **ポートを指定してリモートからローカルへファイルをコピーする**:
   ```bash
   scp -P 2222 user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

4. **ディレクトリを再帰的にコピーする**:
   ```bash
   scp -r /path/to/local/directory user@remote_host:/path/to/remote/
   ```

## ヒント
- `scp`を使用する際は、SSH接続が可能であることを確認してください。
- 大量のファイルを転送する場合は、`-v`オプションを使って進行状況を確認すると便利です。
- 転送先のパスが正しいことを事前に確認し、誤ってファイルを上書きしないように注意しましょう。