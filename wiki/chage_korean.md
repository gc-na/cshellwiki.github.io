# [리눅스] C Shell (csh) chage 사용법: 사용자 비밀번호 만료 정보 관리

## Overview
`chage` 명령은 리눅스 시스템에서 사용자의 비밀번호 만료 정보를 관리하는 데 사용됩니다. 이 명령을 통해 사용자의 비밀번호 만료일, 경고 기간 등을 설정할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
chage [옵션] [인수]
```

## Common Options
- `-l`: 사용자의 비밀번호 만료 정보를 표시합니다.
- `-m`: 비밀번호 변경 후 최소 일수를 설정합니다.
- `-M`: 비밀번호의 최대 사용 기간을 설정합니다.
- `-I`: 비밀번호가 만료된 후 비활성화되기까지의 일수를 설정합니다.
- `-W`: 비밀번호 만료 전에 사용자에게 경고하는 일수를 설정합니다.

## Common Examples
- 사용자의 비밀번호 만료 정보 확인:
  ```bash
  chage -l username
  ```

- 비밀번호 최소 변경 일수를 7일로 설정:
  ```bash
  chage -m 7 username
  ```

- 비밀번호 최대 사용 기간을 30일로 설정:
  ```bash
  chage -M 30 username
  ```

- 비밀번호 만료 후 비활성화까지의 일수를 14일로 설정:
  ```bash
  chage -I 14 username
  ```

- 비밀번호 만료 5일 전에 경고하도록 설정:
  ```bash
  chage -W 5 username
  ```

## Tips
- 비밀번호 정책을 설정할 때는 사용자에게 충분한 경고 기간을 제공하는 것이 좋습니다.
- 주기적으로 비밀번호 만료 정보를 확인하여 보안성을 유지하세요.
- 시스템 관리자는 `chage` 명령을 사용하여 사용자 계정의 보안을 강화할 수 있습니다.