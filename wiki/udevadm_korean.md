# [리눅스] Bash udevadm 사용법: udev 장치 관리

## Overview
`udevadm` 명령어는 리눅스 시스템에서 장치 관리와 관련된 작업을 수행하는 도구입니다. 이 명령어는 udev 데몬과 상호작용하여 시스템에 연결된 장치의 정보를 관리하고, 장치의 이벤트를 모니터링하며, 장치 규칙을 관리하는 데 사용됩니다.

## Usage
기본적인 구문은 다음과 같습니다:
```
udevadm [options] [arguments]
```

## Common Options
- `info`: 특정 장치에 대한 정보를 표시합니다.
- `trigger`: 모든 장치에 대해 udev 규칙을 트리거합니다.
- `settle`: 모든 장치 이벤트가 처리될 때까지 대기합니다.
- `control`: udev 데몬을 제어합니다 (예: 시작, 중지).
- `monitor`: 장치 이벤트를 실시간으로 모니터링합니다.

## Common Examples
1. 특정 장치 정보 확인:
   ```bash
   udevadm info --query=all --name=/dev/sda
   ```

2. 모든 장치에 대해 udev 규칙 트리거:
   ```bash
   udevadm trigger
   ```

3. 장치 이벤트 대기:
   ```bash
   udevadm settle
   ```

4. udev 데몬 상태 확인:
   ```bash
   udevadm control --status
   ```

5. 실시간 장치 이벤트 모니터링:
   ```bash
   udevadm monitor
   ```

## Tips
- `udevadm` 명령어를 사용할 때는 루트 권한이 필요할 수 있습니다.
- 장치 정보를 확인할 때는 `/dev` 경로를 정확하게 지정해야 합니다.
- `udevadm monitor`를 사용하여 실시간으로 장치 이벤트를 확인하면, 시스템에서 발생하는 장치 관련 문제를 진단하는 데 유용합니다.