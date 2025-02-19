# [리눅스] C Shell (csh) curl 사용법: 웹에서 데이터 전송 및 다운로드

## Overview
curl 명령어는 URL을 통해 데이터를 전송하거나 다운로드하는 데 사용됩니다. 다양한 프로토콜을 지원하며, 웹 API와의 상호작용이나 파일 다운로드에 유용합니다.

## Usage
curl의 기본 구문은 다음과 같습니다:

```csh
curl [options] [arguments]
```

## Common Options
- `-O`: 원본 파일 이름으로 파일을 다운로드합니다.
- `-L`: 리다이렉션을 따라갑니다.
- `-I`: HTTP 헤더만 가져옵니다.
- `-d`: POST 요청을 보낼 때 데이터를 전송합니다.
- `-u`: 사용자 인증 정보를 제공합니다.

## Common Examples
- 웹 페이지 다운로드:
```csh
curl -O http://example.com/file.txt
```

- 리다이렉션을 따라가며 다운로드:
```csh
curl -L -O http://example.com/redirect
```

- HTTP 헤더 가져오기:
```csh
curl -I http://example.com
```

- POST 요청으로 데이터 전송:
```csh
curl -d "param1=value1&param2=value2" http://example.com/api
```

- 사용자 인증을 통한 요청:
```csh
curl -u username:password http://example.com/protected
```

## Tips
- curl 명령어는 다양한 프로토콜을 지원하므로, 필요에 따라 적절한 옵션을 선택하세요.
- API와 상호작용할 때는 `-H` 옵션을 사용하여 헤더를 추가할 수 있습니다.
- 다운로드 중 진행 상황을 확인하려면 `-#` 옵션을 사용해 보세요.