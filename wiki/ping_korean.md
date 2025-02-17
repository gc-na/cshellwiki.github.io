# [리눅스] Bash ping 사용법: 네트워크 연결 확인

## Overview
`ping` 명령은 네트워크 연결을 확인하고, 특정 호스트와의 통신이 가능한지를 테스트하는 데 사용됩니다. 이 명령은 ICMP(Internet Control Message Protocol) 에코 요청을 보내고, 응답 시간을 측정하여 네트워크 상태를 진단합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
ping [옵션] [대상]
```

## Common Options
- `-c [횟수]`: 지정한 횟수만큼 패킷을 전송합니다.
- `-i [초]`: 패킷 전송 간격을 설정합니다.
- `-t [TTL]`: 패킷의 생존 시간(Time To Live)을 설정합니다.
- `-s [크기]`: 전송할 패킷의 크기를 설정합니다.

## Common Examples
- 기본 사용법 (지정한 호스트에 ping 전송):
```bash
ping google.com
```

- 5회만 ping 전송:
```bash
ping -c 5 google.com
```

- 패킷 크기를 128바이트로 설정하여 ping 전송:
```bash
ping -s 128 google.com
```

- 2초 간격으로 ping 전송:
```bash
ping -i 2 google.com
```

## Tips
- `ping` 명령을 사용할 때는 대상 호스트가 ICMP 요청을 허용하는지 확인하세요. 일부 서버는 보안상의 이유로 ICMP 요청을 차단할 수 있습니다.
- 네트워크 문제를 진단할 때는 `ping` 명령의 응답 시간을 주의 깊게 살펴보세요. 응답 시간이 길거나 패킷 손실이 발생하면 네트워크에 문제가 있을 수 있습니다.
- `ping` 명령은 네트워크의 기본적인 연결 상태를 확인하는 데 유용하지만, 더 복잡한 문제를 해결하기 위해서는 다른 도구와 함께 사용하는 것이 좋습니다.