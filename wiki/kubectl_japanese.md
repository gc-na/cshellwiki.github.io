# [Linux] Bash kubectl 使用法: Kubernetesクラスターを管理する

## Overview
`kubectl`はKubernetesクラスターを管理するためのコマンドラインツールです。このコマンドを使用することで、ポッド、サービス、デプロイメントなどのリソースを操作し、クラスターの状態を確認することができます。

## Usage
基本的な構文は以下の通りです。

```
kubectl [options] [arguments]
```

## Common Options
- `get`: リソースの一覧を取得します。
- `describe`: 特定のリソースの詳細情報を表示します。
- `apply`: マニフェストファイルを適用してリソースを作成または更新します。
- `delete`: 指定したリソースを削除します。
- `logs`: ポッドのログを表示します。

## Common Examples
以下は、`kubectl`の一般的な使用例です。

### リソースの一覧を取得
```bash
kubectl get pods
```

### 特定のポッドの詳細情報を表示
```bash
kubectl describe pod <pod-name>
```

### マニフェストファイルを適用
```bash
kubectl apply -f deployment.yaml
```

### ポッドを削除
```bash
kubectl delete pod <pod-name>
```

### ポッドのログを表示
```bash
kubectl logs <pod-name>
```

## Tips
- `kubectl`コマンドは、`--namespace`オプションを使用して特定の名前空間を指定できます。
- よく使うコマンドはエイリアスを設定して短縮することができます。
- `kubectl get`コマンドに`-o wide`オプションを追加すると、より詳細な情報が得られます。