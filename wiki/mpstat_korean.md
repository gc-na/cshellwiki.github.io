# [리눅스] Bash mpstat 사용법: CPU 사용량 모니터링

## Overview
`mpstat` 명령은 시스템의 CPU 사용량을 모니터링하고, 각 CPU 코어의 성능 통계를 제공합니다. 이 명령은 멀티코어 시스템에서 CPU의 부하를 분석하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
mpstat [옵션] [인수]
```

## Common Options
- `-P ALL`: 모든 CPU 코어의 통계를 표시합니다.
- `-u`: CPU 사용량을 퍼센트로 표시합니다.
- `-h`: 출력 결과를 사람이 읽기 쉬운 형식으로 표시합니다.
- `interval`: 통계 업데이트 간격(초)을 설정합니다.
- `count`: 통계를 수집할 횟수를 지정합니다.

## Common Examples
- 모든 CPU 코어의 사용량을 1초 간격으로 5회 표시:
  ```bash
  mpstat -P ALL 1 5
  ```

- CPU 사용량을 퍼센트로 표시:
  ```bash
  mpstat -u 1 5
  ```

- 사람이 읽기 쉬운 형식으로 CPU 통계 표시:
  ```bash
  mpstat -h 1
  ```

## Tips
- `mpstat` 명령은 시스템 성능 문제를 진단하는 데 유용하므로, 주기적으로 모니터링하는 것이 좋습니다.
- 여러 옵션을 조합하여 필요한 정보를 효율적으로 수집할 수 있습니다.
- 출력 결과를 파일로 저장하려면 리다이렉션을 사용하세요:
  ```bash
  mpstat -P ALL 1 5 > cpu_usage.txt
  ```