# [리눅스] C Shell (csh) scp 사용법: 원격 서버 간 파일 전송

## Overview
`scp` 명령은 Secure Copy Protocol의 약자로, 네트워크를 통해 파일을 안전하게 복사하는 데 사용됩니다. 이 명령은 SSH 프로토콜을 기반으로 하여 데이터를 암호화하여 전송합니다.

## Usage
기본적인 `scp` 명령의 구문은 다음과 같습니다.

```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: 디렉토리를 재귀적으로 복사합니다.
- `-P`: 원격 호스트의 포트를 지정합니다. (대문자 P)
- `-p`: 원본 파일의 수정 시간과 접근 권한을 유지합니다.
- `-q`: 진행 상태를 표시하지 않습니다.
- `-C`: 전송할 데이터에 대해 압축을 사용합니다.

## Common Examples
다음은 `scp` 명령의 몇 가지 일반적인 예입니다.

1. **로컬 파일을 원격 서버로 복사하기**
   ```bash
   scp localfile.txt user@remotehost:/path/to/destination/
   ```

2. **원격 서버에서 로컬로 파일 복사하기**
   ```bash
   scp user@remotehost:/path/to/remotefile.txt /local/destination/
   ```

3. **디렉토리를 재귀적으로 복사하기**
   ```bash
   scp -r localdirectory/ user@remotehost:/path/to/destination/
   ```

4. **특정 포트를 사용하여 파일 복사하기**
   ```bash
   scp -P 2222 localfile.txt user@remotehost:/path/to/destination/
   ```

## Tips
- `scp`를 사용할 때는 항상 원격 서버의 사용자 이름과 호스트 이름을 정확히 입력해야 합니다.
- 대량의 파일을 전송할 때는 `-C` 옵션을 사용하여 전송 속도를 개선할 수 있습니다.
- 보안을 위해 SSH 키를 사용하여 비밀번호 입력 없이 파일을 전송할 수 있습니다.