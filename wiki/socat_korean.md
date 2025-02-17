# [리눅스] Bash socat 사용법: 데이터 전송 및 변환

## Overview
socat은 소켓을 통해 데이터를 전송하고 변환하는 강력한 도구입니다. 이 명령은 네트워크 연결을 설정하거나 파일과 프로세스 간의 데이터 흐름을 관리하는 데 유용합니다.

## Usage
socat의 기본 구문은 다음과 같습니다:

```bash
socat [options] [arguments]
```

## Common Options
- `-u`: 비차단 모드로 작동합니다.
- `-v`: 자세한 출력을 활성화합니다.
- `TCP:<host>:<port>`: 지정된 호스트와 포트에 TCP 연결을 설정합니다.
- `UDP:<host>:<port>`: 지정된 호스트와 포트에 UDP 연결을 설정합니다.
- `FILE:<filename>`: 파일을 소스 또는 대상으로 사용합니다.

## Common Examples
1. **TCP 서버 생성**:
   ```bash
   socat TCP-LISTEN:1234,fork EXEC:/bin/cat
   ```
   이 명령은 포트 1234에서 TCP 서버를 생성하고, 연결된 클라이언트의 입력을 `/bin/cat` 프로세스로 전달합니다.

2. **TCP 클라이언트로 연결**:
   ```bash
   socat - TCP:example.com:80
   ```
   이 명령은 `example.com`의 80번 포트에 TCP 연결을 설정합니다.

3. **파일을 소켓으로 전송**:
   ```bash
   socat FILE:myfile.txt TCP:localhost:1234
   ```
   이 명령은 `myfile.txt` 파일의 내용을 로컬 호스트의 1234번 포트로 전송합니다.

4. **UDP 통신 설정**:
   ```bash
   socat -u UDP-RECVFROM:1234,fork STDOUT
   ```
   이 명령은 포트 1234에서 UDP 패킷을 수신하고, 수신한 데이터를 표준 출력으로 출력합니다.

## Tips
- socat은 다양한 프로토콜을 지원하므로, 필요한 경우 TCP와 UDP를 적절히 선택하세요.
- `-v` 옵션을 사용하여 디버깅 시 더 많은 정보를 얻을 수 있습니다.
- 보안이 중요한 경우, socat을 SSH와 함께 사용하여 암호화된 연결을 설정할 수 있습니다.