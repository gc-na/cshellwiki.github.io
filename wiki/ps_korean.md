# [리눅스] C Shell (csh) ps 사용법: 프로세스 상태 보기

## Overview
`ps` 명령은 현재 실행 중인 프로세스의 상태를 보여주는 유용한 도구입니다. 이 명령을 사용하면 시스템에서 어떤 프로세스가 실행되고 있는지, 각 프로세스의 PID(프로세스 ID) 및 상태 등을 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
ps [options] [arguments]
```

## Common Options
- `-e`: 모든 프로세스를 나열합니다.
- `-f`: 전체 포맷으로 프로세스 정보를 표시합니다.
- `-u [user]`: 특정 사용자가 실행한 프로세스를 표시합니다.
- `-p [pid]`: 특정 PID를 가진 프로세스를 표시합니다.
- `-l`: 긴 형식으로 프로세스 정보를 표시합니다.

## Common Examples
- 모든 프로세스 나열하기:
  ```csh
  ps -e
  ```

- 특정 사용자 프로세스 보기:
  ```csh
  ps -u username
  ```

- 특정 PID의 프로세스 정보 보기:
  ```csh
  ps -p 1234
  ```

- 전체 형식으로 프로세스 정보 보기:
  ```csh
  ps -ef
  ```

- 긴 형식으로 프로세스 정보 보기:
  ```csh
  ps -l
  ```

## Tips
- `ps` 명령은 기본적으로 현재 셸 세션의 프로세스만 보여주므로, 시스템의 모든 프로세스를 보려면 `-e` 옵션을 사용하는 것이 좋습니다.
- 프로세스 상태를 주기적으로 확인하고 싶다면, `watch` 명령과 함께 사용할 수 있습니다.
- `ps` 명령의 출력 결과를 `grep`과 함께 사용하여 특정 프로세스를 쉽게 찾을 수 있습니다.