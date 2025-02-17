# [台灣] Bash docker 使用法: 管理容器和映像檔

## Overview
Docker 是一個開源平台，讓開發者能夠自動化應用程式的部署、擴展和管理。它使用容器技術來打包應用程式及其依賴，確保在不同環境中都能一致地運行。

## Usage
基本語法如下：
```bash
docker [options] [arguments]
```

## Common Options
- `run`: 創建並啟動一個新的容器。
- `ps`: 列出當前正在運行的容器。
- `images`: 列出本地的所有映像檔。
- `rm`: 刪除一個或多個容器。
- `rmi`: 刪除一個或多個映像檔。

## Common Examples
1. **啟動一個新的容器**
   ```bash
   docker run -d --name my_container nginx
   ```
   這條命令會在背景中啟動一個名為 `my_container` 的 Nginx 容器。

2. **列出正在運行的容器**
   ```bash
   docker ps
   ```
   這條命令會顯示所有當前運行的容器。

3. **查看本地映像檔**
   ```bash
   docker images
   ```
   這條命令會列出所有本地可用的映像檔。

4. **刪除容器**
   ```bash
   docker rm my_container
   ```
   這條命令會刪除名為 `my_container` 的容器。

5. **刪除映像檔**
   ```bash
   docker rmi nginx
   ```
   這條命令會刪除名為 `nginx` 的映像檔。

## Tips
- 在使用 `docker run` 時，加入 `-it` 參數可以讓你進入容器的交互式終端。
- 定期清理不再使用的容器和映像檔，以節省磁碟空間。
- 使用 Docker Compose 來管理多個容器的應用程式，可以簡化配置和啟動過程。