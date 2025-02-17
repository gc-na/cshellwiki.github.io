# [리눅스] Bash vigr 사용법: 파일을 안전하게 편집하기

## Overview
`vigr` 명령은 시스템의 `/etc/passwd` 및 `/etc/group` 파일과 같은 중요한 파일을 안전하게 편집할 수 있도록 도와주는 도구입니다. 이 명령은 파일을 열기 전에 잠금을 설정하여 다른 프로세스가 동시에 파일을 수정하지 못하도록 합니다.

## Usage
기본 구문은 다음과 같습니다:
```
vigr [options] [arguments]
```

## Common Options
- `-f, --file`: 편집할 파일을 지정합니다. 기본적으로 `/etc/passwd` 파일이 열립니다.
- `-s, --safe`: 안전 모드로 실행하여 파일을 잠급니다.
- `-h, --help`: 도움말 정보를 표시합니다.

## Common Examples
1. 기본적으로 `/etc/passwd` 파일을 편집하기:
   ```bash
   vigr
   ```

2. 특정 파일을 편집하기 (예: `/etc/group`):
   ```bash
   vigr -f /etc/group
   ```

3. 안전 모드로 파일 편집하기:
   ```bash
   vigr -s
   ```

## Tips
- `vigr`를 사용할 때는 항상 중요한 시스템 파일을 편집하기 전에 백업을 만들어 두는 것이 좋습니다.
- 편집 후에는 항상 파일의 문법 오류를 확인하여 시스템의 안정성을 유지하세요.
- `vigr`는 vi 편집기를 사용하므로 vi 명령어에 익숙해지는 것이 유용합니다.