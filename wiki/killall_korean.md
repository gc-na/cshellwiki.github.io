# [리눅스] C Shell (csh) killall 사용법: 프로세스 종료

## Overview
`killall` 명령은 지정된 이름의 모든 프로세스를 종료하는 데 사용됩니다. 이 명령은 시스템에서 특정 프로세스를 신속하게 중지해야 할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
killall [옵션] [프로세스 이름]
```

## Common Options
- `-u [사용자]`: 특정 사용자가 소유한 프로세스만 종료합니다.
- `-s [신호]`: 종료할 때 보낼 신호를 지정합니다. 기본값은 `TERM`입니다.
- `-v`: 종료된 프로세스에 대한 정보를 자세히 출력합니다.

## Common Examples
- 모든 `firefox` 프로세스 종료:
  ```csh
  killall firefox
  ```

- 특정 사용자(`username`)의 모든 `python` 프로세스 종료:
  ```csh
  killall -u username python
  ```

- `SIGKILL` 신호를 사용하여 `myapp` 프로세스 강제 종료:
  ```csh
  killall -s SIGKILL myapp
  ```

- 종료된 프로세스에 대한 자세한 정보 출력:
  ```csh
  killall -v myservice
  ```

## Tips
- `killall` 명령을 사용할 때는 프로세스 이름을 정확히 입력해야 합니다. 잘못된 이름을 입력하면 아무런 작업도 수행되지 않습니다.
- 중요한 프로세스를 종료하기 전에 항상 확인하세요. 데이터 손실이 발생할 수 있습니다.
- `-v` 옵션을 사용하여 종료된 프로세스를 확인하면, 어떤 프로세스가 종료되었는지 쉽게 알 수 있습니다.