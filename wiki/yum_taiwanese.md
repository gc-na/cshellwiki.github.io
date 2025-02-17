# [Linux] Bash yum 使用方式: 軟體包管理工具

## Overview
`yum`（Yellowdog Updater, Modified）是一個在基於 RPM 的 Linux 發行版中使用的包管理工具。它可以用來安裝、更新、卸載和管理軟體包，並自動處理依賴性問題。

## Usage
基本語法如下：
```bash
yum [options] [arguments]
```

## Common Options
- `install`：安裝指定的軟體包。
- `remove`：卸載指定的軟體包。
- `update`：更新已安裝的軟體包到最新版本。
- `search`：搜尋可用的軟體包。
- `info`：顯示指定軟體包的詳細資訊。
- `list`：列出可用或已安裝的軟體包。

## Common Examples
以下是一些常見的 `yum` 使用範例：

1. 安裝一個軟體包：
   ```bash
   yum install httpd
   ```

2. 卸載一個軟體包：
   ```bash
   yum remove httpd
   ```

3. 更新所有已安裝的軟體包：
   ```bash
   yum update
   ```

4. 搜尋可用的軟體包：
   ```bash
   yum search nginx
   ```

5. 顯示某個軟體包的資訊：
   ```bash
   yum info vim
   ```

6. 列出所有已安裝的軟體包：
   ```bash
   yum list installed
   ```

## Tips
- 在執行 `yum` 命令之前，建議先使用 `yum check-update` 來檢查可用的更新。
- 使用 `-y` 選項可以自動回答所有提示，適合批次處理：
  ```bash
  yum -y install git
  ```
- 定期清理快取可以釋放磁碟空間，使用以下命令：
  ```bash
  yum clean all
  ```