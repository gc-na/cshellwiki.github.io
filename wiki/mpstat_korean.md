# [리눅스] C Shell (csh) mpstat 사용법: CPU 통계 모니터링

## Overview
mpstat 명령어는 시스템의 CPU 사용량을 모니터링하고, 각 CPU의 성능 통계를 출력하는 도구입니다. 이를 통해 시스템의 부하를 분석하고, 성능 문제를 진단하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
mpstat [options] [arguments]
```

## Common Options
- `-P ALL`: 모든 CPU의 통계를 표시합니다.
- `-u`: CPU 사용률을 보여줍니다.
- `-r`: 메모리 통계를 표시합니다.
- `-h`: 출력 형식을 사람이 읽기 쉽게 합니다.

## Common Examples
다음은 mpstat 명령어의 몇 가지 일반적인 사용 예입니다.

1. 모든 CPU의 사용률을 표시합니다:
   ```bash
   mpstat -P ALL
   ```

2. CPU 사용률을 1초 간격으로 5번 출력합니다:
   ```bash
   mpstat 1 5
   ```

3. CPU 사용률과 메모리 통계를 함께 표시합니다:
   ```bash
   mpstat -u -r
   ```

4. 사람이 읽기 쉬운 형식으로 CPU 통계를 출력합니다:
   ```bash
   mpstat -h
   ```

## Tips
- 시스템의 성능 문제를 진단할 때, mpstat의 출력을 주기적으로 모니터링하는 것이 좋습니다.
- 여러 CPU가 있는 시스템에서는 `-P ALL` 옵션을 사용하여 각 CPU의 성능을 개별적으로 분석하세요.
- mpstat와 함께 다른 시스템 모니터링 도구(예: vmstat, iostat)를 사용하면 더 포괄적인 성능 분석이 가능합니다.