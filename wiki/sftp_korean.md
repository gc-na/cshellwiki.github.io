# [리눅스] Bash sftp 사용법: 파일 전송을 위한 안전한 프로토콜

## Overview
`sftp`는 SSH 파일 전송 프로토콜(SFTP)을 사용하여 안전하게 파일을 전송하고 관리하는 명령어입니다. 이 명령어는 원격 서버와의 파일 전송을 암호화하여 보안을 강화합니다.

## Usage
기본 구문은 다음과 같습니다:
```
sftp [options] [user@]host
```

## Common Options
- `-P` : 포트 번호를 지정합니다.
- `-o` : SSH 옵션을 설정합니다.
- `-b` : 배치 모드에서 파일을 전송합니다.
- `-q` : 조용한 모드로 실행하여 출력 메시지를 줄입니다.

## Common Examples
1. 원격 서버에 연결하기:
   ```bash
   sftp user@hostname
   ```

2. 특정 포트로 연결하기:
   ```bash
   sftp -P 2222 user@hostname
   ```

3. 파일 업로드하기:
   ```bash
   sftp user@hostname
   put localfile.txt
   ```

4. 파일 다운로드하기:
   ```bash
   sftp user@hostname
   get remotefile.txt
   ```

5. 여러 파일을 한 번에 업로드하기:
   ```bash
   sftp user@hostname
   mput *.txt
   ```

## Tips
- 항상 최신 버전의 SSH와 SFTP 클라이언트를 사용하는 것이 좋습니다.
- 중요한 파일을 전송할 때는 전송 후 파일의 무결성을 확인하세요.
- SFTP 세션을 종료할 때는 `bye` 또는 `exit` 명령어를 사용하세요.