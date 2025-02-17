# [Linux] Bash socat 使用法: データの転送と変換

## Overview
`socat`（"SOcket CAT"の略）は、データの転送と変換を行うための強力なツールです。ネットワーク接続やファイル、プロセス間でのデータの送受信を簡単に行うことができます。

## Usage
基本的な構文は以下の通りです。

```bash
socat [options] [arguments]
```

## Common Options
- `-u`: データを非同期に送信します。
- `-v`: 詳細な出力を表示します。
- `TCP:<host>:<port>`: 指定したホストとポートへのTCP接続を作成します。
- `UDP:<host>:<port>`: 指定したホストとポートへのUDP接続を作成します。
- `FILE:<filename>`: 指定したファイルをソースまたはデスティネーションとして使用します。

## Common Examples
以下は`socat`の一般的な使用例です。

### TCP接続の作成
指定したホストとポートにTCP接続を作成します。

```bash
socat TCP:example.com:80 -
```

### UDP接続の作成
指定したホストとポートにUDP接続を作成します。

```bash
socat UDP:example.com:1234 -
```

### ファイルからデータを読み込む
ファイルの内容をTCP接続で送信します。

```bash
socat TCP:example.com:80 FILE:data.txt
```

### プロセス間通信
標準入力からデータを受け取り、別のプロセスに送信します。

```bash
socat -u EXEC:"command",pty,stderr -
```

## Tips
- `-v`オプションを使用して、デバッグ時にデータの流れを確認することができます。
- 複数の接続を同時に処理する場合は、`fork`オプションを利用すると便利です。
- `socat`は非常に柔軟性があるため、用途に応じて様々な組み合わせで使用できます。