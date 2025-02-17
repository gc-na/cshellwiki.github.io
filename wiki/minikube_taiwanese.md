# [台灣] Bash minikube 使用方法: 管理本地 Kubernetes 環境

## Overview
minikube 是一個工具，讓開發者能夠在本地環境中輕鬆地運行 Kubernetes。它提供了一個簡單的方式來啟動和管理一個單節點的 Kubernetes 集群，方便開發和測試。

## Usage
基本語法如下：
```
minikube [options] [arguments]
```

## Common Options
- `start`: 啟動 minikube 集群。
- `stop`: 停止 minikube 集群。
- `delete`: 刪除 minikube 集群。
- `status`: 顯示 minikube 集群的狀態。
- `kubectl`: 用於執行 kubectl 命令的簡便方式。

## Common Examples
啟動 minikube 集群：
```bash
minikube start
```

停止 minikube 集群：
```bash
minikube stop
```

刪除 minikube 集群：
```bash
minikube delete
```

檢查 minikube 集群狀態：
```bash
minikube status
```

使用 kubectl 執行命令：
```bash
minikube kubectl -- get pods -A
```

## Tips
- 確保你的系統滿足 minikube 的要求，特別是虛擬化技術。
- 使用 `minikube addons` 命令來啟用或禁用附加功能，例如 Dashboard。
- 定期更新 minikube 以獲得最新的功能和修復。