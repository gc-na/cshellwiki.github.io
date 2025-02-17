# [리눅스] Bash wget 사용법: 웹에서 파일 다운로드

## Overview
`wget`은 웹에서 파일을 다운로드하는 데 사용되는 명령어입니다. HTTP, HTTPS, FTP 프로토콜을 지원하며, 비대화형으로 작동하여 백그라운드에서 파일을 다운로드할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
wget [options] [arguments]
```

## Common Options
- `-O [파일명]`: 다운로드한 파일의 이름을 지정합니다.
- `-c`: 중단된 다운로드를 재개합니다.
- `-r`: 디렉토리와 그 하위 파일을 재귀적으로 다운로드합니다.
- `-q`: 조용한 모드로, 진행 상황을 표시하지 않습니다.
- `--limit-rate=[속도]`: 다운로드 속도를 제한합니다.

## Common Examples
- 기본 파일 다운로드:
```bash
wget http://example.com/file.zip
```

- 파일 이름 지정하여 다운로드:
```bash
wget -O myfile.zip http://example.com/file.zip
```

- 중단된 다운로드 재개:
```bash
wget -c http://example.com/file.zip
```

- 디렉토리 재귀 다운로드:
```bash
wget -r http://example.com/directory/
```

- 조용한 모드로 다운로드:
```bash
wget -q http://example.com/file.zip
```

## Tips
- 다운로드 속도를 제한하려면 `--limit-rate` 옵션을 사용하여 네트워크 사용량을 조절하세요.
- 대량의 파일을 다운로드할 때는 `-r` 옵션을 사용하여 전체 웹사이트를 다운로드할 수 있지만, 서버에 부담을 주지 않도록 주의하세요.
- 다운로드가 완료된 후 파일의 무결성을 확인하기 위해 체크섬을 사용하는 것이 좋습니다.