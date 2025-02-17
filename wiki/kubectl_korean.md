# [리눅스] Bash kubectl 사용법: Kubernetes 클러스터 관리

## Overview
`kubectl`은 Kubernetes 클러스터와 상호작용하기 위한 명령줄 도구입니다. 이 명령어를 사용하여 클러스터의 리소스를 관리하고, 배포 및 상태 확인을 수행할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
kubectl [options] [arguments]
```

## Common Options
- `get`: 클러스터의 리소스를 조회합니다.
- `apply`: 리소스의 상태를 정의하는 YAML 파일을 적용합니다.
- `delete`: 클러스터에서 리소스를 삭제합니다.
- `describe`: 특정 리소스에 대한 상세 정보를 표시합니다.
- `logs`: 파드의 로그를 출력합니다.

## Common Examples
- 클러스터의 모든 파드 목록 조회:
```bash
kubectl get pods
```

- 특정 네임스페이스의 서비스 목록 조회:
```bash
kubectl get services -n my-namespace
```

- YAML 파일을 사용하여 배포 적용:
```bash
kubectl apply -f deployment.yaml
```

- 특정 파드의 상세 정보 보기:
```bash
kubectl describe pod my-pod
```

- 파드의 로그 확인:
```bash
kubectl logs my-pod
```

## Tips
- `kubectl` 명령어에 `--help` 옵션을 추가하면 각 명령어에 대한 도움말을 볼 수 있습니다.
- 자주 사용하는 명령어는 별도의 스크립트로 만들어 두면 효율적으로 작업할 수 있습니다.
- 네임스페이스를 자주 사용하는 경우, `kubectl config set-context` 명령어로 기본 네임스페이스를 설정해 두면 편리합니다.