# [리눅스] Bash scp 사용법: 원격 서버 간 파일 전송

## Overview
`scp` (Secure Copy Protocol) 명령은 네트워크를 통해 파일을 안전하게 복사하는 데 사용됩니다. SSH 프로토콜을 기반으로 하여 데이터 전송 중 보안을 제공합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: 디렉토리를 재귀적으로 복사합니다.
- `-P`: 원격 호스트의 포트를 지정합니다. (대문자 P)
- `-p`: 파일의 수정 시간 및 접근 시간을 유지합니다.
- `-q`: 진행 상태를 표시하지 않습니다.
- `-C`: 전송 중 데이터 압축을 활성화합니다.

## Common Examples
- 로컬 파일을 원격 서버로 복사하기:
  ```bash
  scp localfile.txt user@remotehost:/path/to/destination/
  ```

- 원격 서버에서 로컬로 파일 복사하기:
  ```bash
  scp user@remotehost:/path/to/remotefile.txt /local/destination/
  ```

- 디렉토리를 원격 서버로 복사하기:
  ```bash
  scp -r /local/directory user@remotehost:/path/to/destination/
  ```

- 특정 포트를 사용하여 원격 서버로 파일 복사하기:
  ```bash
  scp -P 2222 localfile.txt user@remotehost:/path/to/destination/
  ```

## Tips
- 대량의 파일을 전송할 때 `-C` 옵션을 사용하여 전송 속도를 향상시킬 수 있습니다.
- `-v` 옵션을 추가하면 전송 과정에서의 디버깅 정보를 확인할 수 있어 문제 해결에 도움이 됩니다.
- SSH 키를 사용하여 비밀번호 입력 없이 자동으로 파일을 전송할 수 있습니다.