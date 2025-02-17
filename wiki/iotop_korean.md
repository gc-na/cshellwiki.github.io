# [리눅스] Bash iotop 사용법: 디스크 I/O 모니터링

## Overview
iotop은 시스템에서 디스크 I/O를 사용하는 프로세스를 모니터링하는 도구입니다. 이 명령어를 사용하면 어떤 프로세스가 디스크에 가장 많은 작업을 수행하고 있는지 실시간으로 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
iotop [options] [arguments]
```

## Common Options
- `-o`, `--only`: I/O를 발생시키고 있는 프로세스만 표시합니다.
- `-b`, `--batch`: 배치 모드로 실행하여 출력 결과를 표준 출력으로 보냅니다.
- `-n NUM`, `--iter NUM`: NUM회 반복 후 종료합니다.
- `-d SEC`, `--delay SEC`: 각 업데이트 사이의 지연 시간을 초 단위로 설정합니다.

## Common Examples
- 기본 iotop 실행:
```bash
iotop
```

- I/O를 발생시키고 있는 프로세스만 표시:
```bash
iotop -o
```

- 배치 모드로 5초마다 업데이트:
```bash
iotop -b -d 5
```

- 10회 반복 후 종료:
```bash
iotop -n 10
```

## Tips
- iotop을 사용하기 위해서는 root 권한이 필요합니다. `sudo`를 사용하여 실행하세요.
- 시스템의 I/O 사용량을 모니터링할 때, iotop을 다른 모니터링 도구와 함께 사용하는 것이 유용합니다.
- 특정 프로세스의 I/O 성능 문제를 진단할 때, iotop의 출력 결과를 주의 깊게 분석하세요.