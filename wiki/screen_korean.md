# [리눅스] Bash screen 사용법: 터미널 세션 관리

## Overview
`screen` 명령어는 여러 개의 터미널 세션을 관리할 수 있게 해주는 유틸리티입니다. 이를 통해 사용자는 세션을 분리하고, 재접속하며, 백그라운드에서 작업을 계속할 수 있습니다. 특히 원격 서버에서 작업할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
screen [options] [arguments]
```

## Common Options
- `-S [session_name]`: 세션 이름을 지정합니다.
- `-d -r [session_name]`: 분리된 세션을 재접속합니다.
- `-list`: 현재 실행 중인 세션 목록을 표시합니다.
- `-X [command]`: 지정된 세션에 명령을 보냅니다.

## Common Examples
- 새로운 세션 시작:
  ```bash
  screen -S mysession
  ```
- 현재 실행 중인 세션 목록 보기:
  ```bash
  screen -list
  ```
- 분리된 세션 재접속:
  ```bash
  screen -d -r mysession
  ```
- 세션 종료:
  ```bash
  exit
  ```

## Tips
- 세션 이름을 지정하면 여러 세션을 쉽게 관리할 수 있습니다.
- `Ctrl + A`를 누른 후 `D`를 눌러 세션을 분리할 수 있습니다.
- 세션에 재접속할 때는 항상 세션 이름을 확인하세요.