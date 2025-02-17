# [리눅스] Bash iostat 사용법: 시스템 I/O 통계 모니터링

## Overview
`iostat` 명령어는 시스템의 입출력(I/O) 통계를 모니터링하는 데 사용됩니다. 이 도구는 CPU 사용량과 블록 장치의 I/O 통계를 제공하여 시스템 성능을 분석하고 문제를 진단하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
iostat [options] [arguments]
```

## Common Options
- `-c`: CPU 통계만 표시합니다.
- `-d`: 블록 장치의 I/O 통계만 표시합니다.
- `-x`: 확장된 통계를 표시합니다.
- `-t`: 시간 스탬프를 포함하여 출력합니다.
- `interval`: 통계를 출력할 간격(초)을 설정합니다.
- `count`: 출력할 통계의 횟수를 지정합니다.

## Common Examples
1. 기본 I/O 통계 보기:
   ```bash
   iostat
   ```

2. CPU 통계만 표시:
   ```bash
   iostat -c
   ```

3. 블록 장치의 I/O 통계 표시:
   ```bash
   iostat -d
   ```

4. 2초 간격으로 5번 통계 출력:
   ```bash
   iostat 2 5
   ```

5. 확장된 통계 보기:
   ```bash
   iostat -x
   ```

## Tips
- `iostat` 명령어를 주기적으로 실행하여 시스템의 I/O 성능 변화를 모니터링하세요.
- CPU와 I/O 통계를 함께 분석하면 시스템 성능 문제를 더 잘 이해할 수 있습니다.
- `iostat`의 출력 결과를 로그 파일에 저장하여 장기적인 성능 추세를 분석할 수 있습니다.