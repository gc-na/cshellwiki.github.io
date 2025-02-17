# [리눅스] Bash curl 사용법: 웹에서 데이터 전송 및 수신

## Overview
curl 명령어는 URL을 통해 데이터를 전송하거나 수신하는 데 사용되는 강력한 도구입니다. HTTP, HTTPS, FTP 등 다양한 프로토콜을 지원하며, API와의 상호작용에도 자주 사용됩니다.

## Usage
curl의 기본 구문은 다음과 같습니다:

```bash
curl [options] [arguments]
```

## Common Options
- `-X, --request <command>`: 사용할 HTTP 메서드 지정 (예: GET, POST).
- `-d, --data <data>`: POST 요청 시 전송할 데이터 지정.
- `-H, --header <header>`: 사용자 정의 헤더 추가.
- `-o, --output <file>`: 응답 내용을 파일로 저장.
- `-I, --head`: HTTP 헤더만 요청.

## Common Examples
1. **웹 페이지 가져오기**
   ```bash
   curl https://www.example.com
   ```

2. **POST 요청 보내기**
   ```bash
   curl -X POST -d "name=John&age=30" https://www.example.com/api
   ```

3. **헤더 추가하기**
   ```bash
   curl -H "Authorization: Bearer your_token" https://www.example.com/api
   ```

4. **응답을 파일로 저장하기**
   ```bash
   curl -o response.html https://www.example.com
   ```

5. **HTTP 헤더만 요청하기**
   ```bash
   curl -I https://www.example.com
   ```

## Tips
- API와 상호작용할 때는 `-H` 옵션을 사용하여 필요한 인증 헤더를 추가하세요.
- `-o` 옵션을 사용하여 응답을 파일로 저장하면, 나중에 쉽게 참조할 수 있습니다.
- `-v` 옵션을 추가하면 요청과 응답의 상세 정보를 볼 수 있어 디버깅에 유용합니다.