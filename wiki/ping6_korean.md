# [리눅스] Bash ping6 사용법: IPv6 네트워크 연결 확인

## Overview
ping6 명령어는 IPv6 주소를 가진 호스트와의 연결을 확인하고, 네트워크의 응답 시간을 측정하는 데 사용됩니다. 이 명령어는 네트워크 문제를 진단하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
ping6 [옵션] [인수]
```

## Common Options
- `-c <count>`: 전송할 패킷 수를 지정합니다.
- `-i <interval>`: 패킷 전송 간격을 설정합니다.
- `-s <size>`: 전송할 패킷의 크기를 지정합니다.
- `-W <timeout>`: 응답 대기 시간을 설정합니다.

## Common Examples
- 기본 ping6 사용 예:
  ```bash
  ping6 google.com
  ```

- 특정 패킷 수 전송:
  ```bash
  ping6 -c 4 google.com
  ```

- 패킷 크기 지정:
  ```bash
  ping6 -s 128 google.com
  ```

- 응답 대기 시간 설정:
  ```bash
  ping6 -W 2 google.com
  ```

## Tips
- 네트워크 문제를 진단할 때, 여러 호스트에 대해 ping6을 실행하여 응답 시간을 비교하세요.
- IPv6 주소를 직접 입력하여 특정 호스트에 대한 연결을 테스트할 수 있습니다.
- 방화벽 설정이 ping6의 응답에 영향을 줄 수 있으므로, 방화벽 규칙을 확인하는 것이 좋습니다.