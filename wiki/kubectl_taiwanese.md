# [台灣] Bash kubectl 使用方式: 管理 Kubernetes 叢集

## 概述
`kubectl` 是 Kubernetes 的命令列工具，主要用於與 Kubernetes 叢集進行互動。透過 `kubectl`，使用者可以部署應用程式、檢查叢集狀態以及管理叢集資源。

## 使用方式
基本語法如下：
```bash
kubectl [options] [arguments]
```

## 常見選項
- `get`: 獲取資源的列表或詳細資訊。
- `apply`: 應用配置變更到資源。
- `delete`: 刪除指定的資源。
- `describe`: 顯示資源的詳細資訊。
- `logs`: 查看 Pod 的日誌。

## 常見範例
1. 獲取所有 Pod 的列表：
   ```bash
   kubectl get pods
   ```

2. 應用配置檔案：
   ```bash
   kubectl apply -f deployment.yaml
   ```

3. 刪除特定的 Pod：
   ```bash
   kubectl delete pod my-pod
   ```

4. 顯示某個服務的詳細資訊：
   ```bash
   kubectl describe service my-service
   ```

5. 查看某個 Pod 的日誌：
   ```bash
   kubectl logs my-pod
   ```

## 小提示
- 使用 `kubectl get all` 可以一次性獲取所有資源的列表，方便快速檢查叢集狀態。
- 在進行更改之前，建議使用 `kubectl apply --dry-run=client -f <file>` 來模擬應用配置，確保不會意外更改叢集狀態。
- 定期使用 `kubectl cluster-info` 檢查叢集的健康狀態。