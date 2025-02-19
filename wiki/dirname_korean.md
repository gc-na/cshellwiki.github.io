# [리눅스] C Shell (csh) dirname 사용법: 경로에서 디렉토리 이름 추출

## Overview
`dirname` 명령어는 주어진 경로에서 디렉토리 이름을 추출하는 데 사용됩니다. 이 명령어는 파일 경로를 처리할 때 유용하며, 경로의 마지막 구성 요소를 제거하여 상위 디렉토리 경로를 반환합니다.

## Usage
기본 구문은 다음과 같습니다:
```
dirname [options] [arguments]
```

## Common Options
- `-z`: 빈 문자열을 입력으로 받을 때, 빈 문자열을 반환합니다.
- `--help`: 사용법을 보여줍니다.
- `--version`: 버전 정보를 표시합니다.

## Common Examples
다음은 `dirname` 명령어의 몇 가지 일반적인 예입니다.

1. 기본 사용법:
   ```csh
   dirname /home/user/documents/file.txt
   ```
   출력: `/home/user/documents`

2. 상대 경로 사용:
   ```csh
   dirname ./projects/csh/README.md
   ```
   출력: `./projects/csh`

3. 여러 경로 처리:
   ```csh
   dirname /usr/local/bin/script.sh /var/log/syslog
   ```
   출력:
   ```
   /usr/local/bin
   /var/log
   ```

## Tips
- `dirname` 명령어는 스크립트에서 경로를 동적으로 처리할 때 매우 유용합니다.
- 여러 경로를 한 번에 처리할 수 있으므로, 반복적인 작업을 줄이는 데 도움이 됩니다.
- `basename` 명령어와 함께 사용하면 파일 이름과 경로를 쉽게 분리할 수 있습니다.