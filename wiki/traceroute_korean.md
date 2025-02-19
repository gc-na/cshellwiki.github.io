# [리눅스] C Shell (csh) traceroute 사용법: 네트워크 경로 추적

## Overview
traceroute 명령은 네트워크에서 데이터 패킷이 목적지에 도달하기까지 거치는 경로를 추적하는 데 사용됩니다. 이 명령은 각 중간 노드의 IP 주소와 응답 시간을 보여주어 네트워크 문제를 진단하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
traceroute [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: 최대 TTL(Time To Live) 값을 설정합니다.
- `-n`: 호스트 이름 대신 IP 주소를 표시합니다.
- `-q <nqueries>`: 각 홉에 대해 보낼 쿼리 수를 설정합니다.
- `-w <waittime>`: 응답을 기다리는 시간을 설정합니다.

## Common Examples
- 기본 traceroute 사용:
  ```bash
  traceroute example.com
  ```

- IP 주소를 사용하여 traceroute 실행:
  ```bash
  traceroute 192.168.1.1
  ```

- 최대 TTL 값을 15로 설정하여 traceroute 실행:
  ```bash
  traceroute -m 15 example.com
  ```

- 호스트 이름 대신 IP 주소만 표시:
  ```bash
  traceroute -n example.com
  ```

## Tips
- traceroute 결과를 분석할 때, 응답 시간이 긴 홉을 주의 깊게 살펴보세요. 이는 네트워크 병목 현상을 나타낼 수 있습니다.
- 여러 번 실행하여 결과를 비교하면 일관된 패턴을 찾는 데 도움이 됩니다.
- 방화벽이나 보안 설정으로 인해 일부 홉이 응답하지 않을 수 있으므로, 이를 염두에 두고 분석하세요.