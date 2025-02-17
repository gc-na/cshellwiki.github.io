# [리눅스] Bash find 사용법: 파일 이름 찾기

## Overview
`find` 명령어는 파일 시스템 내에서 특정 조건에 맞는 파일이나 디렉토리를 검색하는 데 사용됩니다. 이 명령어는 다양한 옵션을 통해 검색 조건을 세밀하게 조정할 수 있어 매우 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
find [옵션] [인수]
```

## Common Options
- `-name`: 특정 이름을 가진 파일을 찾습니다.
- `-type`: 파일의 유형을 지정합니다. 예를 들어, `f`는 일반 파일, `d`는 디렉토리를 의미합니다.
- `-size`: 파일 크기에 따라 검색합니다. 예를 들어, `+100M`은 100MB보다 큰 파일을 찾습니다.
- `-mtime`: 파일의 수정 시간을 기준으로 검색합니다. 예를 들어, `-mtime -7`은 최근 7일 이내에 수정된 파일을 찾습니다.
- `-exec`: 찾은 파일에 대해 특정 명령을 실행합니다.

## Common Examples
1. 특정 이름의 파일 찾기:
   ```bash
   find /path/to/search -name "example.txt"
   ```

2. 특정 유형의 파일 찾기 (디렉토리):
   ```bash
   find /path/to/search -type d -name "mydir"
   ```

3. 100MB보다 큰 파일 찾기:
   ```bash
   find /path/to/search -size +100M
   ```

4. 최근 7일 이내에 수정된 파일 찾기:
   ```bash
   find /path/to/search -mtime -7
   ```

5. 찾은 파일 삭제하기:
   ```bash
   find /path/to/search -name "*.tmp" -exec rm {} \;
   ```

## Tips
- 검색할 경로를 명확히 지정하여 검색 속도를 높이세요.
- `-print` 옵션을 사용하여 찾은 파일 목록을 출력할 수 있습니다.
- `-maxdepth` 옵션을 사용하여 검색 깊이를 제한하면 성능을 개선할 수 있습니다.