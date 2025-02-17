# [Linux] Bash groupmod の使い方: グループの変更

## Overview
`groupmod` コマンドは、既存のグループの属性を変更するために使用されます。このコマンドを使用することで、グループ名やグループID（GID）などを変更することができます。

## Usage
基本的な構文は以下の通りです。

```bash
groupmod [options] [arguments]
```

## Common Options
- `-n, --new-name`: グループの新しい名前を指定します。
- `-g, --gid`: 新しいグループID（GID）を指定します。
- `-h, --help`: ヘルプ情報を表示します。
- `-o, --non-unique`: 既存のグループIDと同じGIDを使用することを許可します。

## Common Examples
以下に、`groupmod` コマンドのいくつかの実用的な例を示します。

### グループ名の変更
グループ名を `oldgroup` から `newgroup` に変更する場合:

```bash
groupmod -n newgroup oldgroup
```

### グループIDの変更
グループIDを `1001` から `1002` に変更する場合:

```bash
groupmod -g 1002 oldgroup
```

### 非一意のGIDの使用
既存のGIDと同じGIDを使用してグループを変更する場合:

```bash
groupmod -o -g 1001 oldgroup
```

## Tips
- グループ名やGIDを変更する前に、影響を受けるユーザーやプロセスを確認してください。
- `groupmod` コマンドを実行するには、通常、管理者権限（root）が必要です。
- 変更後は、`getent group` コマンドを使用して、グループの情報が正しく更新されたか確認すると良いでしょう。