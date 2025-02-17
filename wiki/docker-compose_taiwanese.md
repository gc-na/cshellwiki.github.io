# [台灣] Bash docker-compose 使用法: 管理多個Docker容器

## Overview
`docker-compose` 是一個用於定義和運行多個Docker容器的工具。透過一個簡單的配置文件，使用者可以輕鬆地設定和管理應用程式的服務，讓容器之間的協作變得更加簡單。

## Usage
基本語法如下：
```bash
docker-compose [options] [arguments]
```

## Common Options
- `up`: 啟動服務，並建立所需的容器。
- `down`: 停止並移除容器、網路和卷。
- `build`: 根據配置文件構建或重建服務。
- `logs`: 查看服務的日誌輸出。
- `exec`: 在運行中的容器內執行命令。

## Common Examples
1. 啟動服務：
    ```bash
    docker-compose up
    ```

2. 在背景運行服務：
    ```bash
    docker-compose up -d
    ```

3. 停止服務：
    ```bash
    docker-compose down
    ```

4. 查看日誌：
    ```bash
    docker-compose logs
    ```

5. 在特定服務的容器內執行命令：
    ```bash
    docker-compose exec <service_name> <command>
    ```

## Tips
- 使用 `-d` 選項可以讓服務在背景運行，這樣你可以繼續使用終端機。
- 定期使用 `docker-compose down` 來清理不再需要的容器和資源。
- 在開發過程中，使用 `docker-compose up --build` 可以確保你總是使用最新的映像檔。