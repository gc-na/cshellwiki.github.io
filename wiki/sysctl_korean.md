# [리눅스] Bash sysctl 사용법: 시스템 커널 매개변수 조정

## Overview
`sysctl` 명령은 리눅스 시스템에서 커널 매개변수를 동적으로 조정하고 조회하는 데 사용됩니다. 이 명령을 통해 시스템 성능을 최적화하거나 특정 기능을 활성화/비활성화할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
sysctl [options] [arguments]
```

## Common Options
- `-a`: 모든 커널 매개변수를 나열합니다.
- `-w`: 커널 매개변수를 설정합니다.
- `-n`: 설정된 값을 출력합니다.
- `-p`: 파일에서 매개변수를 읽어 설정합니다.

## Common Examples
- 모든 커널 매개변수 나열하기:
  ```bash
  sysctl -a
  ```

- 특정 매개변수 값 조회하기 (예: `vm.swappiness`):
  ```bash
  sysctl vm.swappiness
  ```

- 커널 매개변수 설정하기 (예: `vm.swappiness` 값을 10으로 설정):
  ```bash
  sysctl -w vm.swappiness=10
  ```

- 설정 파일에서 매개변수 읽어오기:
  ```bash
  sysctl -p
  ```

## Tips
- `sysctl` 명령을 사용하여 시스템 성능을 조정할 때는 변경 사항이 즉시 적용되므로, 신중하게 값을 설정하세요.
- `/etc/sysctl.conf` 파일에 매개변수를 추가하면 시스템 재부팅 시에도 설정이 유지됩니다.
- 변경 후 시스템의 성능을 모니터링하여 적절한 값을 찾는 것이 중요합니다.