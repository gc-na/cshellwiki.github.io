# [Linux] Bash minikube 使用: 启动和管理本地Kubernetes集群

## 概述
minikube 是一个工具，用于在本地机器上快速启动和管理 Kubernetes 集群。它为开发人员提供了一个简单的环境来测试和开发 Kubernetes 应用程序。

## 用法
基本语法如下：
```
minikube [options] [arguments]
```

## 常用选项
- `start`：启动一个新的 minikube 集群。
- `stop`：停止当前运行的 minikube 集群。
- `delete`：删除当前的 minikube 集群。
- `status`：显示当前 minikube 集群的状态。
- `kubectl`：使用 kubectl 命令与 minikube 集群进行交互。

## 常见示例
1. 启动 minikube 集群：
   ```bash
   minikube start
   ```

2. 停止 minikube 集群：
   ```bash
   minikube stop
   ```

3. 删除 minikube 集群：
   ```bash
   minikube delete
   ```

4. 查看 minikube 集群状态：
   ```bash
   minikube status
   ```

5. 使用 kubectl 与 minikube 集群交互：
   ```bash
   kubectl get pods --all-namespaces
   ```

## 提示
- 在启动 minikube 之前，确保你的系统满足所有要求，例如虚拟化支持。
- 使用 `minikube dashboard` 命令可以打开 Kubernetes 仪表板，方便进行可视化管理。
- 定期使用 `minikube update-check` 来检查 minikube 的更新，以确保你使用的是最新版本。