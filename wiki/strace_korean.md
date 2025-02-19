# [리눅스] C Shell (csh) strace 사용법: 시스템 호출 추적

## Overview
`strace` 명령은 프로그램이 수행하는 시스템 호출과 신호를 추적하는 데 사용됩니다. 이를 통해 개발자는 프로그램의 동작을 이해하고, 디버깅 및 성능 분석을 수행할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
strace [options] [arguments]
```

## Common Options
- `-c`: 시스템 호출 통계를 요약하여 보여줍니다.
- `-e trace=SYSCALL`: 특정 시스템 호출만 추적합니다.
- `-p PID`: 이미 실행 중인 프로세스를 추적합니다.
- `-o FILE`: 출력 결과를 지정한 파일에 저장합니다.

## Common Examples
- 기본 사용법: 프로그램의 시스템 호출을 추적합니다.
  ```bash
  strace ls
  ```

- 특정 시스템 호출만 추적하기: `open` 시스템 호출만 추적합니다.
  ```bash
  strace -e trace=open ls
  ```

- 실행 중인 프로세스 추적: PID가 1234인 프로세스를 추적합니다.
  ```bash
  strace -p 1234
  ```

- 출력 결과를 파일에 저장하기: `output.txt` 파일에 결과를 저장합니다.
  ```bash
  strace -o output.txt ls
  ```

- 시스템 호출 통계 요약: 프로그램의 시스템 호출 통계를 보여줍니다.
  ```bash
  strace -c ls
  ```

## Tips
- `strace`를 사용하여 프로그램의 성능 문제를 진단할 수 있습니다.
- 필요한 시스템 호출만 추적하여 출력 결과를 간소화하세요.
- 출력 결과를 파일로 저장하면 나중에 분석하기가 더 쉽습니다.