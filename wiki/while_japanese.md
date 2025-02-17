# [Linux] Bash while の使い方: 繰り返し処理を実行する

## Overview
`while` コマンドは、指定した条件が真である限り、特定のコマンドを繰り返し実行するために使用されます。この構文は、ループ処理を行いたい場合に非常に便利です。

## Usage
基本的な構文は次のとおりです。

```bash
while [ 条件 ]; do
    コマンド
done
```

## Common Options
`while` コマンド自体にはオプションはありませんが、条件式には以下のようなオプションを使用できます。

- `-n`: 文字列が空でない場合に真。
- `-z`: 文字列が空の場合に真。
- `-eq`: 数値が等しい場合に真。
- `-lt`: 数値が小さい場合に真。
- `-gt`: 数値が大きい場合に真。

## Common Examples

### 例1: 簡単なカウンタループ
```bash
count=1
while [ $count -le 5 ]; do
    echo "カウント: $count"
    ((count++))
done
```

### 例2: ユーザー入力を受け付ける
```bash
input=""
while [ "$input" != "exit" ]; do
    read -p "入力してください (exitで終了): " input
    echo "あなたの入力: $input"
done
```

### 例3: ファイルの行を読み込む
```bash
while IFS= read -r line; do
    echo "行: $line"
done < filename.txt
```

## Tips
- `while` ループの中で条件を変更することを忘れないでください。そうしないと、無限ループに陥る可能性があります。
- `break` コマンドを使用して、特定の条件でループを終了することができます。
- `continue` コマンドを使用して、次の反復にスキップすることができます。