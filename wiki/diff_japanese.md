# [UNIX] C Shell (csh) diff 使用法: ファイルの差分を比較する

## Overview
`diff` コマンドは、2つのファイルの内容を比較し、異なる部分を表示するためのツールです。このコマンドを使用することで、変更点や差異を簡単に確認することができます。

## Usage
基本的な構文は以下の通りです。

```csh
diff [options] [arguments]
```

## Common Options
- `-u` : 統一形式で差分を表示します。
- `-c` : コンテキスト形式で差分を表示します。
- `-i` : 大文字と小文字を無視して比較します。
- `-w` : 空白の違いを無視して比較します。

## Common Examples
以下に、`diff` コマンドのいくつかの実用的な例を示します。

### 例1: 基本的なファイル比較
```csh
diff file1.txt file2.txt
```

### 例2: 統一形式での差分表示
```csh
diff -u file1.txt file2.txt
```

### 例3: コンテキスト形式での差分表示
```csh
diff -c file1.txt file2.txt
```

### 例4: 大文字小文字を無視して比較
```csh
diff -i file1.txt file2.txt
```

### 例5: 空白を無視して比較
```csh
diff -w file1.txt file2.txt
```

## Tips
- `diff` コマンドは、スクリプトやプログラムの変更を追跡するのに非常に便利です。
- 出力をファイルにリダイレクトすることで、後で確認できるように保存できます。例えば、`diff file1.txt file2.txt > diff_output.txt` のように使用します。
- `diff` の結果を理解するために、出力の記号（`<` や `>`）の意味を把握しておくと良いでしょう。