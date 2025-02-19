# [리눅스] C Shell (csh) screen 사용법: 터미널 세션 관리

## Overview
`screen` 명령어는 여러 개의 터미널 세션을 관리할 수 있게 해주는 유틸리티입니다. 이를 통해 사용자는 세션을 분리하고, 백그라운드에서 작업을 계속할 수 있으며, 나중에 다시 연결할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
screen [options] [arguments]
```

## Common Options
- `-S <session_name>`: 세션에 이름을 지정합니다.
- `-d -r <session_name>`: 분리된 세션을 다시 연결합니다.
- `-list`: 현재 실행 중인 세션 목록을 보여줍니다.
- `-X <command>`: 특정 세션에 명령을 보냅니다.

## Common Examples
- 새로운 세션 시작하기:
    ```bash
    screen -S mysession
    ```
- 분리된 세션 목록 보기:
    ```bash
    screen -list
    ```
- 특정 세션에 다시 연결하기:
    ```bash
    screen -d -r mysession
    ```
- 세션에서 명령 실행하기:
    ```bash
    screen -S mysession -X stuff 'echo Hello World\n'
    ```

## Tips
- 세션을 분리할 때는 `Ctrl+A`를 누르고 `D`를 눌러주세요.
- 세션 이름을 지정하면 여러 세션을 쉽게 관리할 수 있습니다.
- 세션이 종료되지 않도록 주기적으로 확인하는 것이 좋습니다.