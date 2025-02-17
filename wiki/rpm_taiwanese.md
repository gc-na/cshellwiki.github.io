# [Linux] Bash rpm 使用說明: 管理 RPM 套件

## Overview
`rpm` 是一個用於管理 RPM 套件的命令行工具，主要用於安裝、卸載、升級和查詢 RPM 格式的軟體包。這個工具在基於 RPM 的 Linux 發行版中非常常見，如 Red Hat、CentOS 和 Fedora。

## Usage
基本語法如下：
```
rpm [options] [arguments]
```

## Common Options
- `-i`：安裝一個新的 RPM 套件。
- `-e`：卸載已安裝的 RPM 套件。
- `-U`：升級已安裝的 RPM 套件。
- `-q`：查詢已安裝的 RPM 套件。
- `-l`：列出已安裝套件的檔案。
- `--help`：顯示幫助信息。

## Common Examples
以下是一些常見的 `rpm` 使用範例：

### 安裝一個 RPM 套件
```bash
rpm -i package.rpm
```

### 卸載一個已安裝的套件
```bash
rpm -e package_name
```

### 升級一個已安裝的套件
```bash
rpm -U package.rpm
```

### 查詢已安裝的套件
```bash
rpm -q package_name
```

### 列出已安裝套件的檔案
```bash
rpm -ql package_name
```

## Tips
- 在安裝或升級套件之前，建議先使用 `-q` 選項確認套件是否已安裝。
- 使用 `--nodeps` 選項可以在安裝時忽略依賴性檢查，但這可能會導致系統不穩定，請謹慎使用。
- 定期查詢和清理不再需要的套件，以保持系統的整潔和性能。