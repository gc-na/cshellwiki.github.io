# [리눅스] C Shell (csh) socat 사용법: 소켓 간 데이터 전송

## Overview
socat은 소켓 간에 데이터를 전송하는 강력한 도구입니다. 이 명령어는 다양한 종류의 데이터 스트림을 연결할 수 있으며, 네트워크 통신 및 데이터 전송을 위한 유연한 솔루션을 제공합니다.

## Usage
기본 구문은 다음과 같습니다:
```
socat [options] [arguments]
```

## Common Options
- `-d`: 디버그 모드를 활성화하여 상세한 로그를 출력합니다.
- `-v`: 전송되는 데이터를 출력하여 실시간으로 확인할 수 있습니다.
- `TCP-LISTEN:<port>`: 지정된 포트에서 TCP 연결을 수신합니다.
- `UDP-LISTEN:<port>`: 지정된 포트에서 UDP 연결을 수신합니다.
- `EXEC:<command>`: 지정된 명령어를 실행하고 그 입출력을 연결합니다.

## Common Examples
1. TCP 포트에서 수신하고 다른 포트로 전송하기:
   ```bash
   socat TCP-LISTEN:1234,fork TCP:localhost:5678
   ```

2. 파일을 소켓으로 전송하기:
   ```bash
   socat FILE:/path/to/file TCP:localhost:1234
   ```

3. UDP 소켓을 통해 데이터 전송하기:
   ```bash
   socat UDP-LISTEN:1234,fork EXEC:/path/to/script.sh
   ```

4. 두 개의 터미널 간에 데이터 전송하기:
   ```bash
   socat -d -d pty,link=/tmp/ttyS0,mode=777 pty,link=/tmp/ttyS1,mode=777
   ```

## Tips
- socat을 사용할 때는 포트 충돌을 피하기 위해 사용 중인 포트를 확인하세요.
- 디버그 모드를 활성화하여 문제를 진단하는 데 도움을 받을 수 있습니다.
- 다양한 프로토콜과 옵션을 조합하여 복잡한 네트워크 환경에서도 유연하게 사용할 수 있습니다.