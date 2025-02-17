# [Linux] Bash mv 使用法: ファイルやディレクトリの移動と名前変更

## Overview
`mv` コマンドは、ファイルやディレクトリを移動したり、名前を変更したりするために使用されます。このコマンドは、指定されたソースの位置からターゲットの位置へデータを移動します。

## Usage
基本的な構文は以下の通りです。

```bash
mv [options] [source] [destination]
```

## Common Options
- `-i`: 上書きする前に確認を求める。
- `-u`: ソースがターゲットより新しい場合のみ移動する。
- `-v`: 移動中のファイル名を表示する。
- `-f`: 上書き確認をせずに強制的に移動する。

## Common Examples
以下は、`mv` コマンドの実用的な例です。

1. ファイルの名前を変更する:
   ```bash
   mv oldname.txt newname.txt
   ```

2. ファイルを別のディレクトリに移動する:
   ```bash
   mv file.txt /path/to/destination/
   ```

3. ディレクトリを移動する:
   ```bash
   mv /path/to/source_directory/ /path/to/destination_directory/
   ```

4. 上書き確認を求めるオプションを使用する:
   ```bash
   mv -i file.txt /path/to/destination/
   ```

5. 移動中のファイル名を表示する:
   ```bash
   mv -v file.txt /path/to/destination/
   ```

## Tips
- 移動先のディレクトリが存在しない場合、`mv` コマンドはファイル名を変更しようとしますので、注意が必要です。
- 大量のファイルを移動する場合は、`-v` オプションを使って進行状況を確認すると便利です。
- 上書きのリスクを避けるために、`-i` オプションを使用することをお勧めします。