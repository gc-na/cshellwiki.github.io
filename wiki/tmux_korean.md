# [리눅스] Bash tmux 사용법: 터미널 멀티플렉서

## Overview
tmux는 터미널 멀티플렉서로, 하나의 터미널 세션에서 여러 개의 가상 터미널을 생성하고 관리할 수 있게 해줍니다. 이를 통해 사용자는 여러 작업을 동시에 수행하고, 세션을 분리하거나 재접속할 수 있는 유연성을 가집니다.

## Usage
tmux의 기본 구문은 다음과 같습니다:

```bash
tmux [options] [arguments]
```

## Common Options
- `new`: 새로운 tmux 세션을 생성합니다.
- `attach`: 기존 세션에 연결합니다.
- `detach`: 현재 세션에서 분리합니다.
- `list-sessions`: 현재 실행 중인 세션 목록을 표시합니다.
- `kill-session`: 특정 세션을 종료합니다.

## Common Examples
- 새로운 tmux 세션 생성하기:
  ```bash
  tmux new -s mysession
  ```

- 기존 세션에 연결하기:
  ```bash
  tmux attach -t mysession
  ```

- 현재 세션에서 분리하기 (Ctrl + b, d):
  ```bash
  # Ctrl + b를 누른 후 d를 누릅니다.
  ```

- 실행 중인 세션 목록 보기:
  ```bash
  tmux list-sessions
  ```

- 특정 세션 종료하기:
  ```bash
  tmux kill-session -t mysession
  ```

## Tips
- tmux의 세션을 분리한 후에도 작업이 계속 실행되므로, 서버에서 장시간 실행되는 작업을 관리할 때 유용합니다.
- 단축키를 활용하여 작업 효율성을 높일 수 있습니다. 예를 들어, `Ctrl + b` 후 `c`를 눌러 새로운 창을 생성할 수 있습니다.
- tmux.conf 파일을 설정하여 개인의 작업 스타일에 맞게 tmux의 기본 동작을 커스터마이즈할 수 있습니다.