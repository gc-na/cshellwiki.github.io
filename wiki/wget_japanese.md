# [Linux] Bash wget の使い方: ウェブからファイルをダウンロードする

## Overview
`wget` コマンドは、ウェブからファイルをダウンロードするための強力なツールです。HTTP、HTTPS、FTPなどのプロトコルを使用して、リモートサーバーからデータを取得することができます。

## Usage
基本的な構文は以下の通りです。

```bash
wget [options] [arguments]
```

## Common Options
- `-O [filename]`: ダウンロードしたファイルを指定した名前で保存します。
- `-q`: 静かなモードで実行し、出力を抑えます。
- `-c`: 中断したダウンロードを再開します。
- `--limit-rate=[rate]`: ダウンロード速度を制限します。
- `-r`: 再帰的にダウンロードします。

## Common Examples
以下は、`wget` コマンドのいくつかの実用的な例です。

### 1. 単一のファイルをダウンロードする
```bash
wget https://example.com/file.zip
```

### 2. 特定の名前でファイルを保存する
```bash
wget -O myfile.zip https://example.com/file.zip
```

### 3. ダウンロードを再開する
```bash
wget -c https://example.com/largefile.zip
```

### 4. 再帰的にウェブサイトをダウンロードする
```bash
wget -r https://example.com/
```

### 5. ダウンロード速度を制限する
```bash
wget --limit-rate=200k https://example.com/largefile.zip
```

## Tips
- 大きなファイルをダウンロードする際は、`-c` オプションを使って中断したダウンロードを再開できるので便利です。
- サーバーに負担をかけないように、`--limit-rate` オプションでダウンロード速度を調整することをお勧めします。
- 再帰的にダウンロードする場合は、`-r` オプションを使用し、必要に応じて `-np`（親ディレクトリを追跡しない）オプションを追加すると良いでしょう。