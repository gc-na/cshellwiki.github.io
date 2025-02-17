# [中文] Bash docker-compose 用法: 管理 Docker 容器的工具

## 概述
docker-compose 是一个用于定义和运行多容器 Docker 应用程序的工具。通过使用 YAML 文件来配置应用程序的服务，用户可以轻松地管理多个容器的生命周期。

## 用法
基本语法如下：
```bash
docker-compose [options] [arguments]
```

## 常用选项
- `up`：启动服务并创建容器。
- `down`：停止并删除容器、网络和卷。
- `build`：构建或重建服务。
- `logs`：查看服务的日志输出。
- `ps`：列出当前运行的容器。

## 常见示例
1. 启动服务：
   ```bash
   docker-compose up
   ```

2. 在后台启动服务：
   ```bash
   docker-compose up -d
   ```

3. 停止并删除容器：
   ```bash
   docker-compose down
   ```

4. 查看服务日志：
   ```bash
   docker-compose logs
   ```

5. 构建服务：
   ```bash
   docker-compose build
   ```

## 小贴士
- 使用 `-d` 选项可以在后台运行容器，方便管理。
- 定期使用 `docker-compose down` 清理不再需要的容器和网络，以节省资源。
- 在开发过程中，可以使用 `docker-compose up --build` 来确保每次启动时都构建最新的镜像。