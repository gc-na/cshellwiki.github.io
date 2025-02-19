# [리눅스] C Shell (csh) udevadm 사용법: 장치 관리 명령

## 개요
`udevadm` 명령은 리눅스 시스템에서 장치 관리와 관련된 작업을 수행하는 데 사용됩니다. 이 명령은 udev 시스템의 상태를 확인하고, 장치의 속성을 관리하며, 장치 이벤트를 모니터링하는 데 유용합니다.

## 사용법
기본 구문은 다음과 같습니다:
```
udevadm [옵션] [인수]
```

## 일반 옵션
- `info`: 특정 장치에 대한 정보를 표시합니다.
- `trigger`: 장치 이벤트를 트리거하여 udev 규칙을 실행합니다.
- `settle`: 현재의 장치 이벤트가 완료될 때까지 대기합니다.
- `control`: udev 데몬의 동작을 제어합니다.

## 일반 예제
장치에 대한 정보를 확인하는 예제:
```bash
udevadm info --query=all --name=/dev/sda
```

장치 이벤트를 트리거하는 예제:
```bash
udevadm trigger
```

현재의 장치 이벤트가 완료될 때까지 대기하는 예제:
```bash
udevadm settle
```

## 팁
- `udevadm info` 명령을 사용하여 특정 장치의 속성을 쉽게 확인할 수 있습니다.
- 장치 이벤트를 모니터링할 때는 `udevadm monitor` 명령을 사용하여 실시간으로 이벤트를 확인할 수 있습니다.
- udev 규칙을 수정한 후에는 `udevadm control --reload-rules` 명령을 사용하여 변경 사항을 적용해야 합니다.