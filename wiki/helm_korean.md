# [리눅스] Bash helm 사용법: 패키지 관리 도구

## Overview
Helm은 Kubernetes에서 애플리케이션을 관리하기 위한 패키지 관리자입니다. Helm을 사용하면 애플리케이션을 쉽게 배포하고, 관리하며, 버전 관리를 할 수 있습니다. Helm 차트라는 패키지 형식을 통해 복잡한 애플리케이션을 간단하게 설치하고 구성할 수 있습니다.

## Usage
Helm의 기본 구문은 다음과 같습니다:

```bash
helm [options] [arguments]
```

## Common Options
- `install`: 차트를 설치합니다.
- `upgrade`: 이미 설치된 차트를 업그레이드합니다.
- `rollback`: 이전 버전으로 롤백합니다.
- `list`: 설치된 릴리스를 나열합니다.
- `uninstall`: 설치된 릴리스를 제거합니다.

## Common Examples
- **차트 설치하기**
  ```bash
  helm install my-release my-chart
  ```
  이 명령은 `my-chart`라는 차트를 `my-release`라는 이름으로 설치합니다.

- **차트 업그레이드하기**
  ```bash
  helm upgrade my-release my-chart
  ```
  이 명령은 이미 설치된 `my-release`를 `my-chart`로 업그레이드합니다.

- **설치된 릴리스 목록 보기**
  ```bash
  helm list
  ```
  이 명령은 현재 설치된 모든 릴리스를 나열합니다.

- **릴리스 롤백하기**
  ```bash
  helm rollback my-release 1
  ```
  이 명령은 `my-release`를 이전 버전인 1로 롤백합니다.

- **릴리스 제거하기**
  ```bash
  helm uninstall my-release
  ```
  이 명령은 `my-release`를 제거합니다.

## Tips
- Helm 차트를 사용하기 전에 항상 최신 버전으로 업데이트하세요.
- 차트를 설치할 때 `--values` 옵션을 사용하여 사용자 정의 값을 제공할 수 있습니다.
- 릴리스를 관리할 때는 적절한 네임스페이스를 지정하여 충돌을 피하세요.