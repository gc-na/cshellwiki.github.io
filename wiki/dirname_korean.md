# [리눅스] Bash dirname 사용법: 파일 경로에서 디렉토리 이름 추출

## Overview
`dirname` 명령어는 주어진 파일 경로에서 디렉토리 이름을 추출하는 데 사용됩니다. 이 명령어는 파일의 전체 경로를 입력받아 해당 파일이 위치한 디렉토리의 경로를 반환합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
dirname [options] [arguments]
```

## Common Options
- `-z`, `--zero`: 입력이 널 문자로 구분된 경우 사용합니다.
- `--help`: 사용법 정보를 출력합니다.
- `--version`: 버전 정보를 출력합니다.

## Common Examples
다음은 `dirname` 명령어의 몇 가지 실용적인 예입니다.

1. 기본 사용법:
   ```bash
   dirname /home/user/documents/file.txt
   ```
   출력: `/home/user/documents`

2. 상대 경로 사용:
   ```bash
   dirname ./projects/code/script.sh
   ```
   출력: `./projects/code`

3. 여러 경로에서 디렉토리 이름 추출:
   ```bash
   dirname /var/log/syslog /etc/hosts
   ```
   출력:
   ```
   /var/log
   /etc
   ```

4. 널 문자로 구분된 입력 사용:
   ```bash
   printf "/home/user/file1.txt\0/home/user/file2.txt\0" | xargs -0 dirname
   ```
   출력:
   ```
   /home/user
   /home/user
   ```

## Tips
- `dirname` 명령어는 스크립트에서 파일 경로를 처리할 때 유용하게 사용될 수 있습니다.
- 경로가 상대적일 경우, 현재 작업 디렉토리에 따라 결과가 달라질 수 있으므로 주의하세요.
- `dirname`과 함께 `basename` 명령어를 사용하면 파일 이름과 디렉토리 경로를 쉽게 분리할 수 있습니다.