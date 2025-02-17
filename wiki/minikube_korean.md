# [리눅스] Bash minikube 사용법: 로컬 Kubernetes 클러스터 관리

## Overview
minikube는 로컬에서 Kubernetes 클러스터를 쉽게 설정하고 관리할 수 있도록 도와주는 도구입니다. 개발 및 테스트 환경에서 Kubernetes를 활용할 수 있게 해주며, 다양한 클라우드 환경에서의 배포를 시뮬레이션할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```
minikube [options] [arguments]
```

## Common Options
- `start`: 새로운 Minikube 클러스터를 시작합니다.
- `stop`: 현재 실행 중인 Minikube 클러스터를 중지합니다.
- `delete`: Minikube 클러스터를 삭제합니다.
- `status`: 현재 Minikube 클러스터의 상태를 확인합니다.
- `kubectl`: kubectl 명령어를 사용하여 클러스터와 상호작용합니다.

## Common Examples
- Minikube 클러스터 시작하기:
    ```bash
    minikube start
    ```

- Minikube 클러스터 상태 확인하기:
    ```bash
    minikube status
    ```

- Minikube 클러스터 중지하기:
    ```bash
    minikube stop
    ```

- Minikube 클러스터 삭제하기:
    ```bash
    minikube delete
    ```

- kubectl을 사용하여 Pod 목록 보기:
    ```bash
    minikube kubectl -- get pods
    ```

## Tips
- Minikube를 시작하기 전에 시스템 요구사항을 확인하세요. VM이나 Docker가 설치되어 있어야 합니다.
- 클러스터를 자주 삭제하고 생성하는 경우, `minikube start --delete-on-exit` 옵션을 사용하여 종료 시 자동으로 삭제할 수 있습니다.
- Minikube의 다양한 드라이버를 활용하여 성능을 최적화하세요. 예를 들어, VirtualBox, Docker, Hyperkit 등 다양한 드라이버를 지원합니다.