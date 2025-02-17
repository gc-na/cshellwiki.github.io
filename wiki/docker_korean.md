# [리눅스] Bash docker 사용법: 컨테이너 관리 명령어

## Overview
Docker는 소프트웨어를 컨테이너라는 가벼운 가상 환경에서 실행할 수 있게 해주는 플랫폼입니다. 이를 통해 개발자는 애플리케이션을 쉽게 배포하고 관리할 수 있습니다.

## Usage
Docker 명령어의 기본 구문은 다음과 같습니다.

```bash
docker [options] [arguments]
```

## Common Options
- `run`: 새로운 컨테이너를 생성하고 실행합니다.
- `ps`: 현재 실행 중인 컨테이너 목록을 보여줍니다.
- `stop`: 실행 중인 컨테이너를 중지합니다.
- `rm`: 중지된 컨테이너를 삭제합니다.
- `images`: 로컬에 저장된 이미지 목록을 보여줍니다.

## Common Examples
- **컨테이너 실행하기**:
  ```bash
  docker run hello-world
  ```
  이 명령어는 "hello-world" 이미지를 사용하여 새로운 컨테이너를 실행합니다.

- **실행 중인 컨테이너 목록 보기**:
  ```bash
  docker ps
  ```
  현재 실행 중인 모든 컨테이너의 목록을 출력합니다.

- **컨테이너 중지하기**:
  ```bash
  docker stop <container_id>
  ```
  `<container_id>`에 해당하는 컨테이너를 중지합니다.

- **중지된 컨테이너 삭제하기**:
  ```bash
  docker rm <container_id>
  ```
  중지된 컨테이너를 삭제합니다.

- **로컬 이미지 목록 보기**:
  ```bash
  docker images
  ```
  로컬에 저장된 모든 Docker 이미지를 나열합니다.

## Tips
- 컨테이너를 실행할 때 `-d` 옵션을 사용하면 백그라운드에서 실행할 수 있습니다.
- `docker-compose`를 사용하면 여러 컨테이너를 쉽게 관리할 수 있습니다.
- 자주 사용하는 명령어는 스크립트로 만들어 두면 편리합니다.