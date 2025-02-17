# [Linux] Bash brew 用法: 管理软件包

## 概述
`brew` 是一个流行的包管理工具，主要用于在 macOS 和 Linux 系统上安装、管理和更新软件包。它简化了软件的安装过程，使用户能够轻松获取和维护各种开发工具和应用程序。

## 用法
基本语法如下：
```bash
brew [options] [arguments]
```

## 常用选项
- `install`：安装指定的软件包。
- `uninstall`：卸载指定的软件包。
- `update`：更新 Homebrew 本身和已安装的软件包。
- `upgrade`：升级已安装的软件包到最新版本。
- `list`：列出已安装的软件包。

## 常见示例
1. 安装软件包：
   ```bash
   brew install wget
   ```

2. 卸载软件包：
   ```bash
   brew uninstall wget
   ```

3. 更新 Homebrew 和软件包：
   ```bash
   brew update
   ```

4. 升级所有已安装的软件包：
   ```bash
   brew upgrade
   ```

5. 列出所有已安装的软件包：
   ```bash
   brew list
   ```

## 小贴士
- 在安装软件包之前，使用 `brew search <package>` 来查找可用的软件包。
- 定期运行 `brew update` 和 `brew upgrade` 以保持软件包的最新状态。
- 使用 `brew info <package>` 查看软件包的详细信息和安装说明。