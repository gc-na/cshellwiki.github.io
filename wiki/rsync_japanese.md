# [Linux] Bash rsync の使い方: ファイルの同期と転送

## Overview
`rsync` コマンドは、ファイルやディレクトリを効率的に同期・転送するためのツールです。ローカルおよびリモートのシステム間でデータをコピーする際に、変更された部分だけを転送するため、帯域幅を節約し、転送速度を向上させます。

## Usage
基本的な構文は以下の通りです。

```bash
rsync [options] [source] [destination]
```

## Common Options
- `-a`: アーカイブモード。ファイルの属性を保持しながらコピーします。
- `-v`: 詳細モード。進行状況を表示します。
- `-z`: 圧縮転送。データを圧縮して転送します。
- `-r`: 再帰的にディレクトリをコピーします。
- `--delete`: 送信先に存在しないファイルを削除します。

## Common Examples
以下に、`rsync` の一般的な使用例を示します。

1. ローカルファイルのコピー:
   ```bash
   rsync -av /path/to/source /path/to/destination
   ```

2. リモートサーバーへのファイル転送:
   ```bash
   rsync -av /path/to/local/file user@remote:/path/to/remote/destination
   ```

3. リモートサーバーからのファイル取得:
   ```bash
   rsync -av user@remote:/path/to/remote/file /path/to/local/destination
   ```

4. ディレクトリを再帰的に同期し、削除オプションを使用:
   ```bash
   rsync -av --delete /path/to/source/ /path/to/destination/
   ```

## Tips
- `-n` オプションを使用して、実行前に何が行われるかを確認できます（ドライラン）。
- 大きなファイルを転送する際は、`-z` オプションを使って圧縮することで、転送時間を短縮できます。
- 定期的なバックアップには、`cron` と組み合わせて自動化することを検討してください。