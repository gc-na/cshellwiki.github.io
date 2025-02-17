# [리눅스] Bash htop 사용법: 시스템 모니터링 도구

## Overview
htop은 시스템의 프로세스와 자원 사용량을 실시간으로 모니터링할 수 있는 대화형 프로세스 뷰어입니다. 이 도구는 CPU, 메모리, 스왑 사용량을 시각적으로 표시하며, 프로세스를 쉽게 관리할 수 있는 기능을 제공합니다.

## Usage
htop의 기본 구문은 다음과 같습니다:

```bash
htop [options] [arguments]
```

## Common Options
- `-h`, `--help`: 도움말을 표시합니다.
- `-s`, `--sort`: 프로세스를 특정 기준으로 정렬합니다.
- `-p`, `--pid`: 특정 프로세스 ID를 모니터링합니다.
- `-u`, `--user`: 특정 사용자의 프로세스만 표시합니다.

## Common Examples
- 기본 htop 실행:
  ```bash
  htop
  ```

- 특정 사용자 프로세스만 보기:
  ```bash
  htop -u username
  ```

- 특정 프로세스 ID 모니터링:
  ```bash
  htop -p 1234
  ```

- CPU 사용량 기준으로 정렬:
  ```bash
  htop -s PERCENT_CPU
  ```

## Tips
- htop에서 F1 키를 눌러 도움말을 확인하고, F10 키로 종료할 수 있습니다.
- 프로세스를 선택한 후 F9 키를 눌러 종료 신호를 보낼 수 있습니다.
- htop의 색상 코드를 이용해 자원 사용량을 쉽게 파악할 수 있습니다.