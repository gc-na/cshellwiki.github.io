# [Linux] Bash helm 使用法: 管理 Kubernetes 應用程式

## Overview
`helm` 是一個 Kubernetes 的套件管理工具，主要用來簡化應用程式的部署和管理。它使用「圖表」(charts) 的概念，讓使用者可以輕鬆地安裝、升級和管理 Kubernetes 應用程式。

## Usage
基本語法如下：
```bash
helm [options] [arguments]
```

## Common Options
- `install`: 安裝一個新的圖表。
- `upgrade`: 升級已安裝的圖表。
- `uninstall`: 卸載已安裝的圖表。
- `list`: 列出已安裝的圖表。
- `repo`: 管理 Helm 圖表的來源庫。

## Common Examples
以下是一些常見的 `helm` 使用範例：

1. 安裝一個新的圖表：
   ```bash
   helm install my-release stable/mysql
   ```

2. 升級已安裝的圖表：
   ```bash
   helm upgrade my-release stable/mysql
   ```

3. 卸載已安裝的圖表：
   ```bash
   helm uninstall my-release
   ```

4. 列出所有已安裝的圖表：
   ```bash
   helm list
   ```

5. 添加一個新的圖表來源庫：
   ```bash
   helm repo add stable https://charts.helm.sh/stable
   ```

## Tips
- 在安裝圖表之前，建議先使用 `helm repo update` 更新圖表來源庫，以確保獲得最新的圖表版本。
- 使用 `--dry-run` 選項可以在實際執行之前模擬安裝過程，幫助檢查配置是否正確。
- 定期使用 `helm list` 檢查已安裝的圖表，保持環境的整潔。