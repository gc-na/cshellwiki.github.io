# [Unix系] C Shell (csh) switch 使用法: 条件分岐を行う

## Overview
`switch` コマンドは、指定した条件に基づいて異なる処理を実行するための制御構造です。主にスクリプト内で条件分岐を行う際に使用されます。

## Usage
基本的な構文は以下の通りです。

```
switch (式)
case 値1:
    コマンド1
    breaksw
case 値2:
    コマンド2
    breaksw
default:
    コマンド3
endsw
```

## Common Options
`switch` コマンドには特別なオプションはありませんが、以下のキーワードが重要です。

- `case`: 条件に一致する場合に実行されるコマンドを定義します。
- `breaksw`: 現在の `switch` 文を終了します。
- `default`: どの `case` にも一致しない場合に実行されるコマンドを定義します。
- `endsw`: `switch` 文の終了を示します。

## Common Examples

### 例1: 基本的な使用法
```csh
set var = "apple"
switch ($var)
case "apple":
    echo "これはリンゴです"
    breaksw
case "banana":
    echo "これはバナナです"
    breaksw
default:
    echo "未知の果物です"
endsw
```

### 例2: 数値の条件分岐
```csh
set num = 2
switch ($num)
case 1:
    echo "数は1です"
    breaksw
case 2:
    echo "数は2です"
    breaksw
case 3:
    echo "数は3です"
    breaksw
default:
    echo "数は1, 2, 3のいずれでもありません"
endsw
```

### 例3: 複数の条件
```csh
set day = "月曜日"
switch ($day)
case "月曜日":
case "火曜日":
    echo "週の始まりです"
    breaksw
case "水曜日":
    echo "週の真ん中です"
    breaksw
default:
    echo "週の後半です"
endsw
```

## Tips
- `switch` 文は、複数の条件を簡潔に処理するのに便利です。特に、同じ処理を行う複数の条件がある場合に有効です。
- `case` の条件は、文字列や数値の比較が可能ですが、正確に一致する必要があります。
- `breaksw` を忘れると、次の `case` にも処理が流れてしまうので注意が必要です。