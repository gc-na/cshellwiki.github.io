# [리눅스] Bash ftp 사용법: 파일 전송을 위한 명령어

## Overview
`ftp` 명령어는 파일 전송 프로토콜(File Transfer Protocol)을 사용하여 네트워크를 통해 파일을 전송하는 데 사용됩니다. 이 명령어를 통해 원격 서버에 연결하고 파일을 업로드하거나 다운로드할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
ftp [options] [arguments]
```

## Common Options
- `-i`: 바이너리 모드로 전송, 파일이 손실되지 않도록 합니다.
- `-n`: 자동 로그인 방지를 위한 옵션입니다.
- `-v`: 자세한 출력을 활성화합니다.
- `-p`: 패시브 모드로 전환하여 방화벽을 통과할 수 있도록 합니다.

## Common Examples
1. 원격 FTP 서버에 연결하기:
   ```bash
   ftp ftp.example.com
   ```

2. 사용자 이름과 비밀번호를 입력하여 연결하기:
   ```bash
   ftp -n ftp.example.com
   user your_username your_password
   ```

3. 파일 다운로드하기:
   ```bash
   get remote_file.txt
   ```

4. 파일 업로드하기:
   ```bash
   put local_file.txt
   ```

5. 디렉토리 목록 보기:
   ```bash
   ls
   ```

## Tips
- FTP를 사용할 때는 보안에 유의하세요. 가능하다면 SFTP(Secure FTP)를 사용하는 것이 좋습니다.
- 파일 전송 모드를 설정할 때는 `binary` 또는 `ascii` 모드를 명확히 지정하세요.
- FTP 서버에 연결 후, `help` 명령어를 입력하면 사용 가능한 모든 명령어 목록을 확인할 수 있습니다.