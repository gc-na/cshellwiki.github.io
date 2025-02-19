# [리눅스] C Shell (csh) tmux 사용법: 터미널 멀티플렉서

## Overview
tmux는 터미널 멀티플렉서로, 사용자가 여러 개의 터미널 세션을 동시에 관리하고 전환할 수 있게 해줍니다. 이를 통해 작업을 더 효율적으로 수행할 수 있습니다.

## Usage
tmux의 기본 구문은 다음과 같습니다:
```bash
tmux [options] [arguments]
```

## Common Options
- `new`: 새로운 tmux 세션을 생성합니다.
- `attach`: 기존 tmux 세션에 연결합니다.
- `detach`: 현재 세션에서 분리합니다.
- `list-sessions`: 현재 실행 중인 모든 tmux 세션을 나열합니다.
- `kill-session`: 특정 세션을 종료합니다.

## Common Examples
- 새로운 tmux 세션 시작하기:
```bash
tmux new -s mysession
```

- 기존 세션에 연결하기:
```bash
tmux attach -t mysession
```

- 현재 세션에서 분리하기:
```bash
tmux detach
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
- 세션 이름을 지정하면 여러 세션을 쉽게 관리할 수 있습니다.
- tmux에서 여러 창을 만들고 쉽게 전환할 수 있으므로, 작업을 분리하여 진행하는 것이 좋습니다.
- 단축키를 활용하여 tmux의 기능을 빠르게 사용할 수 있습니다. 예를 들어, `Ctrl+b`를 누른 후 `c`로 새 창을 만들 수 있습니다.