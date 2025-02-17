# [Linux] Bash continue 使用法: ループを継続する

## Overview
`continue` コマンドは、Bashスクリプトやシェルで使用される制御フローコマンドの一つです。このコマンドは、ループ内で特定の条件が満たされた場合に、現在の反復をスキップし、次の反復に進むために使用されます。

## Usage
基本的な構文は以下の通りです。

```bash
continue [n]
```

ここで、`n` はスキップするループの回数を指定します。省略した場合は、1回の反復がスキップされます。

## Common Options
- `n`: スキップするループの回数を指定します。デフォルトは1です。

## Common Examples

### 例1: 基本的な使用法
次の例では、1から5までの数字をループし、3のときにスキップします。

```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    continue
  fi
  echo $i
done
```
出力:
```
1
2
4
5
```

### 例2: 条件に基づくスキップ
以下の例では、偶数の数字をスキップします。

```bash
for i in {1..10}; do
  if [ $((i % 2)) -eq 0 ]; then
    continue
  fi
  echo $i
done
```
出力:
```
1
3
5
7
9
```

### 例3: ネストされたループでの使用
ネストされたループの中で `continue` を使用する例です。

```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      continue
    fi
    echo "i: $i, j: $j"
  done
done
```
出力:
```
i: 1, j: 1
i: 1, j: 3
i: 2, j: 1
i: 2, j: 3
i: 3, j: 1
i: 3, j: 3
```

## Tips
- `continue` は主に `for`、`while`、`until` ループ内で使用されます。
- 条件を明確に設定することで、意図しない反復をスキップしないように注意してください。
- ネストされたループでは、`continue` がどのループに影響を与えるかを理解しておくことが重要です。