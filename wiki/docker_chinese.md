# [Linux] Bash docker 使用: 管理容器和镜像

## 概述
docker 命令是一个用于管理容器和镜像的工具。它允许用户创建、运行和管理容器化应用程序，使得软件的部署和管理变得更加高效和灵活。

## 用法
基本语法如下：
```bash
docker [options] [arguments]
```

## 常用选项
- `run`: 创建并启动一个新的容器。
- `ps`: 列出当前运行的容器。
- `images`: 列出本地可用的镜像。
- `pull`: 从远程仓库下载镜像。
- `push`: 将本地镜像上传到远程仓库。

## 常见示例
1. **运行一个新的容器**
   ```bash
   docker run hello-world
   ```
   这个命令会下载并运行一个简单的“Hello World”容器。

2. **查看正在运行的容器**
   ```bash
   docker ps
   ```
   该命令列出当前运行的所有容器。

3. **列出所有镜像**
   ```bash
   docker images
   ```
   这个命令显示本地存储的所有镜像。

4. **从远程仓库下载镜像**
   ```bash
   docker pull ubuntu
   ```
   该命令将从 Docker Hub 下载最新的 Ubuntu 镜像。

5. **上传镜像到远程仓库**
   ```bash
   docker push myusername/myimage
   ```
   这个命令将本地镜像上传到指定的远程仓库。

## 提示
- 在使用 `docker run` 时，可以使用 `-d` 选项在后台运行容器。
- 使用 `--rm` 选项可以在容器停止后自动删除容器，节省空间。
- 定期使用 `docker system prune` 来清理未使用的容器和镜像，以保持系统整洁。