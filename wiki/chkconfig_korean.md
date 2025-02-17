# [리눅스] Bash chkconfig 사용법: 서비스 관리 명령어

## Overview
`chkconfig` 명령어는 리눅스 시스템에서 서비스의 실행 수준을 관리하는 데 사용됩니다. 이 명령어를 통해 시스템 부팅 시 어떤 서비스가 시작되고 중지될지를 설정할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
chkconfig [options] [arguments]
```

## Common Options
- `--list`: 현재 설정된 서비스의 상태를 나열합니다.
- `--add`: 새로운 서비스를 추가합니다.
- `--del`: 기존 서비스를 삭제합니다.
- `--level`: 특정 실행 수준에서 서비스의 상태를 설정합니다.

## Common Examples
- 현재 설정된 서비스 목록을 확인하려면:
  ```bash
  chkconfig --list
  ```

- 새로운 서비스를 추가하려면:
  ```bash
  chkconfig --add myservice
  ```

- 특정 서비스의 실행 수준을 설정하려면:
  ```bash
  chkconfig myservice on --level 2345
  ```

- 서비스를 삭제하려면:
  ```bash
  chkconfig --del myservice
  ```

## Tips
- 서비스의 상태를 변경하기 전에 항상 현재 상태를 확인하는 것이 좋습니다.
- 서비스 추가 후, 반드시 서비스가 올바르게 작동하는지 테스트하세요.
- 시스템의 부팅 성능을 최적화하기 위해 필요하지 않은 서비스는 비활성화하는 것이 좋습니다.