# [리눅스] C Shell (csh) hostname 사용법: 호스트 이름 표시 및 설정

## Overview
`hostname` 명령어는 현재 시스템의 호스트 이름을 표시하거나 설정하는 데 사용됩니다. 이 명령어를 통해 네트워크에서 시스템을 식별할 수 있는 이름을 관리할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
hostname [options] [arguments]
```

## Common Options
- `-f`, `--fqdn`: 전체 도메인 이름(Fully Qualified Domain Name)을 표시합니다.
- `-i`: 호스트의 IP 주소를 표시합니다.
- `-s`: 짧은 호스트 이름을 표시합니다.
- `--help`: 사용법을 표시합니다.
- `--version`: 버전 정보를 표시합니다.

## Common Examples
- 현재 호스트 이름 표시:
  ```csh
  hostname
  ```

- 전체 도메인 이름 표시:
  ```csh
  hostname -f
  ```

- 호스트의 IP 주소 표시:
  ```csh
  hostname -i
  ```

- 짧은 호스트 이름 표시:
  ```csh
  hostname -s
  ```

- 호스트 이름 설정:
  ```csh
  hostname new-hostname
  ```

## Tips
- 호스트 이름을 변경한 후에는 시스템을 재부팅하거나 네트워크 서비스를 재시작해야 변경 사항이 적용될 수 있습니다.
- 호스트 이름은 네트워크에서 시스템을 식별하는 중요한 요소이므로, 명확하고 의미 있는 이름을 사용하는 것이 좋습니다.
- `hostname` 명령어를 사용하여 현재 설정된 호스트 이름을 주기적으로 확인하는 것이 좋습니다.