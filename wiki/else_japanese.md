# [Linux] Bash else 使用法: 条件分岐の処理

## Overview
`else` コマンドは、Bash スクリプトにおける条件分岐を実現するための構文の一部です。`if` 文と組み合わせて使用され、条件が満たされない場合に実行されるコマンドを指定します。

## Usage
基本的な構文は以下の通りです。

```bash
if [ 条件 ]; then
    # 条件が真の場合の処理
else
    # 条件が偽の場合の処理
fi
```

## Common Options
`else` 自体にはオプションはありませんが、`if` 文で使用される条件式にはさまざまなオプションがあります。例えば、`-eq`（等しい）、`-ne`（等しくない）、`-lt`（より小さい）、`-gt`（より大きい）などがあります。

## Common Examples

### 例 1: 基本的な条件分岐
```bash
#!/bin/bash
num=10

if [ $num -gt 5 ]; then
    echo "数は5より大きいです。"
else
    echo "数は5以下です。"
fi
```

### 例 2: ファイルの存在確認
```bash
#!/bin/bash
file="example.txt"

if [ -e $file ]; then
    echo "$file は存在します。"
else
    echo "$file は存在しません。"
fi
```

### 例 3: ユーザー入力の確認
```bash
#!/bin/bash
read -p "あなたの名前を入力してください: " name

if [ -z "$name" ]; then
    echo "名前が入力されていません。"
else
    echo "こんにちは、$name さん！"
fi
```

## Tips
- `if` 文と `else` 文を適切にインデントすることで、スクリプトの可読性が向上します。
- 複数の条件を扱う場合は、`elif` を使用して条件を追加できます。
- 条件式には、数値や文字列の比較だけでなく、ファイルの存在確認なども含めることができます。