# [리눅스] Bash tcpdump 사용법: 네트워크 패킷 캡처

## Overview
`tcpdump`는 네트워크 인터페이스를 통해 흐르는 패킷을 캡처하고 분석하는 데 사용되는 강력한 명령어입니다. 주로 네트워크 트래픽을 모니터링하고 문제를 진단하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
tcpdump [options] [arguments]
```

## Common Options
- `-i <interface>`: 패킷을 캡처할 네트워크 인터페이스를 지정합니다.
- `-n`: 호스트 이름을 해석하지 않고 IP 주소로만 표시합니다.
- `-c <count>`: 캡처할 패킷의 수를 지정합니다.
- `-w <file>`: 캡처한 패킷을 파일로 저장합니다.
- `-r <file>`: 저장된 패킷 파일을 읽어 분석합니다.

## Common Examples
- 특정 인터페이스에서 패킷 캡처하기:
```bash
tcpdump -i eth0
```

- IP 주소를 해석하지 않고 패킷 캡처하기:
```bash
tcpdump -i eth0 -n
```

- 10개의 패킷만 캡처하기:
```bash
tcpdump -i eth0 -c 10
```

- 캡처한 패킷을 파일로 저장하기:
```bash
tcpdump -i eth0 -w capture.pcap
```

- 저장된 패킷 파일을 읽어 분석하기:
```bash
tcpdump -r capture.pcap
```

## Tips
- 패킷 캡처를 시작하기 전에 적절한 권한이 필요합니다. 일반적으로 `sudo`를 사용해야 합니다.
- 특정 포트나 프로토콜을 필터링하여 캡처할 수 있습니다. 예를 들어, HTTP 트래픽만 캡처하려면 `tcpdump -i eth0 port 80`을 사용할 수 있습니다.
- 캡처한 패킷의 양이 많을 수 있으므로, 필요한 경우 `-c` 옵션을 사용하여 패킷 수를 제한하는 것이 좋습니다.