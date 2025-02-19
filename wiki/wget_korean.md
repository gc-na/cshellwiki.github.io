# [리눅스] C Shell (csh) wget 사용법: 웹에서 파일 다운로드

## Overview
`wget` 명령어는 웹에서 파일을 다운로드하는 데 사용됩니다. HTTP, HTTPS, FTP 프로토콜을 지원하며, 인터넷에서 파일을 쉽게 가져올 수 있도록 도와줍니다.

## Usage
기본 구문은 다음과 같습니다:
```
wget [옵션] [인수]
```

## Common Options
- `-O [파일명]`: 다운로드한 파일의 이름을 지정합니다.
- `-c`: 중단된 다운로드를 재개합니다.
- `-r`: 재귀적으로 다운로드하여 전체 웹사이트를 가져옵니다.
- `-q`: 조용한 모드로, 진행 상황을 표시하지 않습니다.
- `--limit-rate=[속도]`: 다운로드 속도를 제한합니다.

## Common Examples
- 단일 파일 다운로드:
  ```bash
  wget https://example.com/file.zip
  ```

- 특정 이름으로 파일 다운로드:
  ```bash
  wget -O myfile.zip https://example.com/file.zip
  ```

- 중단된 다운로드 재개:
  ```bash
  wget -c https://example.com/largefile.zip
  ```

- 전체 웹사이트 다운로드:
  ```bash
  wget -r https://example.com
  ```

- 조용한 모드로 다운로드:
  ```bash
  wget -q https://example.com/file.zip
  ```

## Tips
- 대용량 파일을 다운로드할 때는 `-c` 옵션을 사용하여 중단된 다운로드를 쉽게 재개할 수 있습니다.
- 웹사이트를 다운로드할 때는 `-r` 옵션을 사용할 수 있지만, 서버에 과부하를 주지 않도록 주의하세요.
- 다운로드 속도를 제한하려면 `--limit-rate` 옵션을 활용하여 네트워크 사용량을 관리할 수 있습니다.