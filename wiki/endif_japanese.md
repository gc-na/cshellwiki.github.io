# [Linux] Bash endif の使い方: 条件文の終了を示す

## Overview
`endif` コマンドは、Bash スクリプトにおいて条件文の終了を示すために使用されます。このコマンドは、`if` 文と組み合わせて使用され、条件が満たされた場合に実行されるコードブロックの終わりを明示します。

## Usage
基本的な構文は次の通りです。

```bash
endif
```

## Common Options
`endif` コマンド自体にはオプションはありませんが、`if` 文と組み合わせて使用されることが一般的です。

## Common Examples

### 例1: 基本的な条件文
```bash
if [ "$VAR" -eq 1 ]; then
    echo "VARは1です"
endif
```

### 例2: 複数の条件文
```bash
if [ "$VAR" -eq 1 ]; then
    echo "VARは1です"
elif [ "$VAR" -eq 2 ]; then
    echo "VARは2です"
endif
```

### 例3: ネストされた条件文
```bash
if [ "$VAR" -eq 1 ]; then
    echo "VARは1です"
    if [ "$ANOTHER_VAR" -eq 5 ]; then
        echo "ANOTHER_VARは5です"
    endif
endif
```

## Tips
- `endif` は `if` 文の終了を示すため、必ず対応する `if` 文の後に配置してください。
- 複雑な条件文の場合、可読性を高めるためにインデントを使用することをお勧めします。
- スクリプトのデバッグ時には、条件文のブロックが正しく終了しているか確認することが重要です。