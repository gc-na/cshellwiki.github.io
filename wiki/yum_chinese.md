# [Linux] Bash yum 使用方法: 软件包管理工具

## 概述
`yum` 是一个用于在基于 RPM 的 Linux 发行版上管理软件包的命令行工具。它可以帮助用户安装、更新、删除和管理软件包及其依赖关系。

## 用法
基本语法如下：
```
yum [options] [arguments]
```

## 常用选项
- `install`：安装指定的软件包。
- `remove`：删除指定的软件包。
- `update`：更新已安装的软件包。
- `search`：搜索软件包。
- `info`：显示软件包的详细信息。
- `list`：列出可用或已安装的软件包。

## 常见示例
- 安装软件包：
  ```bash
  yum install httpd
  ```
  
- 删除软件包：
  ```bash
  yum remove httpd
  ```

- 更新所有已安装的软件包：
  ```bash
  yum update
  ```

- 搜索软件包：
  ```bash
  yum search nginx
  ```

- 显示软件包信息：
  ```bash
  yum info vim
  ```

- 列出所有可用的软件包：
  ```bash
  yum list available
  ```

## 提示
- 在执行 `yum` 命令时，建议使用 `sudo` 提升权限，确保有足够的权限进行软件包管理。
- 定期更新系统，保持软件包的最新状态，以提高安全性和稳定性。
- 使用 `yum clean all` 命令清理缓存，以释放磁盘空间。