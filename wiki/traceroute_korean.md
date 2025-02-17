# [리눅스] Bash traceroute 사용법: 네트워크 경로 추적

## Overview
traceroute 명령어는 네트워크에서 특정 호스트까지의 경로를 추적하는 데 사용됩니다. 이 명령어는 데이터 패킷이 목적지에 도달하기 위해 거치는 각 중간 라우터의 IP 주소와 응답 시간을 보여줍니다.

## Usage
기본 구문은 다음과 같습니다:
```
traceroute [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: 최대 TTL(Time To Live) 값을 설정합니다.
- `-n`: IP 주소를 숫자로만 표시하여 DNS 조회를 생략합니다.
- `-p <port>`: 특정 포트를 지정하여 트레이스합니다.
- `-w <timeout>`: 각 응답에 대한 타임아웃 시간을 설정합니다.

## Common Examples
1. 기본 traceroute 실행:
   ```bash
   traceroute example.com
   ```

2. 최대 TTL 값을 15로 설정:
   ```bash
   traceroute -m 15 example.com
   ```

3. IP 주소만 표시:
   ```bash
   traceroute -n example.com
   ```

4. 특정 포트를 사용하여 traceroute 실행:
   ```bash
   traceroute -p 80 example.com
   ```

5. 응답 타임아웃을 2초로 설정:
   ```bash
   traceroute -w 2 example.com
   ```

## Tips
- traceroute 명령어는 네트워크 문제를 진단하는 데 유용합니다. 응답 시간이 긴 라우터를 찾아내어 병목 현상을 파악할 수 있습니다.
- DNS 조회를 생략하고 싶다면 `-n` 옵션을 사용하여 결과를 더 빠르게 확인할 수 있습니다.
- traceroute는 방화벽에 의해 차단될 수 있으므로, 접근 권한이 있는 네트워크에서 실행하는 것이 좋습니다.