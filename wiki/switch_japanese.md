# [Linux] Bash switch 使用法: コマンドの切り替え

## Overview
`switch` コマンドは、条件に基づいて異なる処理を実行するための構文を提供します。特に、スクリプト内での条件分岐を簡素化するために使用されます。

## Usage
基本的な構文は次のとおりです。

```
switch [options] [arguments]
```

## Common Options
- `-c` : 条件を指定します。
- `-d` : デフォルトの動作を設定します。
- `-h` : ヘルプを表示します。

## Common Examples
以下に、`switch` コマンドのいくつかの実用的な例を示します。

### 例1: 基本的な条件分岐
```bash
switch $1 in
    start)
        echo "サービスを開始します"
        ;;
    stop)
        echo "サービスを停止します"
        ;;
    *)
        echo "無効なオプションです"
        ;;
esac
```

### 例2: 複数の条件
```bash
switch $1 in
    red)
        echo "色は赤です"
        ;;
    green)
        echo "色は緑です"
        ;;
    blue)
        echo "色は青です"
        ;;
    *)
        echo "色が指定されていません"
        ;;
esac
```

### 例3: デフォルトの動作
```bash
switch $1 in
    yes)
        echo "はいが選択されました"
        ;;
    no)
        echo "いいえが選択されました"
        ;;
    *)
        echo "選択が無効です"
        ;;
esac
```

## Tips
- `switch` コマンドを使用する際は、条件を明確に定義することが重要です。
- デフォルトの動作を設定することで、予期しない入力に対処できます。
- スクリプトの可読性を高めるために、適切なインデントを使用してください。