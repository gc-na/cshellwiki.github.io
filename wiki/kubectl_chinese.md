# [Linux] Bash kubectl 使用指南: 管理 Kubernetes 集群

## 概述
`kubectl` 是 Kubernetes 的命令行工具，用于与 Kubernetes 集群进行交互。通过 `kubectl`，用户可以部署应用、管理集群资源以及查看集群状态等。

## 用法
基本语法如下：
```bash
kubectl [options] [arguments]
```

## 常用选项
- `get`: 获取资源信息。
- `describe`: 显示资源的详细信息。
- `create`: 创建新的资源。
- `delete`: 删除资源。
- `apply`: 应用配置文件中的变更。

## 常见示例
1. 获取所有 Pod 的列表：
   ```bash
   kubectl get pods
   ```

2. 查看特定 Pod 的详细信息：
   ```bash
   kubectl describe pod <pod-name>
   ```

3. 创建一个新的部署：
   ```bash
   kubectl create deployment <deployment-name> --image=<image-name>
   ```

4. 删除一个服务：
   ```bash
   kubectl delete service <service-name>
   ```

5. 应用配置文件：
   ```bash
   kubectl apply -f <config-file.yaml>
   ```

## 提示
- 在执行命令时，可以使用 `--namespace` 选项指定命名空间。
- 使用 `-o` 选项可以改变输出格式，例如 `-o json` 或 `-o yaml`。
- 定期使用 `kubectl get all` 命令来检查集群中所有资源的状态。