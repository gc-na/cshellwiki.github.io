# [리눅스] Bash traceroute6 사용법: IPv6 경로 추적

## Overview
`traceroute6` 명령은 IPv6 네트워크에서 데이터 패킷이 목적지에 도달하기까지 거치는 경로를 추적하는 데 사용됩니다. 이 명령은 네트워크 문제를 진단하고, 패킷이 이동하는 경로를 시각화하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
traceroute6 [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: 최대 TTL(Time To Live) 값을 설정합니다.
- `-p <port>`: 지정된 포트로 패킷을 전송합니다.
- `-n`: 호스트 이름 대신 IP 주소를 표시합니다.
- `-w <timeout>`: 응답 대기 시간을 설정합니다.

## Common Examples
1. 기본 사용법:
   ```bash
   traceroute6 google.com
   ```

2. 최대 TTL 값을 30으로 설정:
   ```bash
   traceroute6 -m 30 google.com
   ```

3. IP 주소만 표시:
   ```bash
   traceroute6 -n google.com
   ```

4. 특정 포트로 패킷 전송:
   ```bash
   traceroute6 -p 80 google.com
   ```

5. 응답 대기 시간을 2초로 설정:
   ```bash
   traceroute6 -w 2 google.com
   ```

## Tips
- `traceroute6` 명령은 네트워크 문제를 진단할 때 유용하므로, 문제가 발생한 경우 먼저 시도해 보세요.
- TTL 값을 조정하여 더 깊은 경로를 추적할 수 있지만, 너무 높은 값은 불필요한 시간을 소모할 수 있습니다.
- IP 주소만 표시하는 `-n` 옵션을 사용하면 결과를 더 빠르게 얻을 수 있습니다.