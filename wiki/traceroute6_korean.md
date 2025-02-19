# [리눅스] C Shell (csh) traceroute6 사용법: IPv6 경로 추적

## Overview
traceroute6 명령은 IPv6 네트워크에서 패킷이 목적지에 도달하기까지 거치는 경로를 추적하는 데 사용됩니다. 이 명령은 네트워크 문제를 진단하고, 특정 호스트에 대한 연결 경로를 시각화하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
traceroute6 [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: 최대 TTL(Time To Live) 값을 설정합니다.
- `-p <port>`: 사용할 포트 번호를 지정합니다.
- `-n`: 호스트 이름 대신 IP 주소를 표시합니다.
- `-q <nqueries>`: 각 홉에 대해 보낼 쿼리 수를 설정합니다.

## Common Examples
다음은 traceroute6 명령의 몇 가지 일반적인 사용 예입니다.

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

4. 특정 포트를 사용하여 경로 추적:
   ```bash
   traceroute6 -p 80 google.com
   ```

5. 각 홉에 대해 3개의 쿼리 전송:
   ```bash
   traceroute6 -q 3 google.com
   ```

## Tips
- traceroute6 명령을 사용할 때, 네트워크 방화벽이 ICMP 패킷을 차단할 수 있으므로, 결과가 예상과 다를 수 있습니다.
- 여러 번 실행하여 결과를 비교하면 네트워크의 안정성을 평가하는 데 도움이 됩니다.
- 특정 목적지에 대한 경로를 추적할 때는 DNS 이름 대신 IP 주소를 사용하는 것이 더 빠를 수 있습니다.