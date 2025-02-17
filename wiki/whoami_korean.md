# [리눅스] Bash whoami 사용법: 현재 사용자 이름 출력

## Overview
`whoami` 명령어는 현재 로그인한 사용자의 이름을 출력합니다. 이 명령어는 시스템에서 현재 사용자가 누구인지 확인할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
whoami [options] [arguments]
```

## Common Options
`whoami` 명령어는 일반적으로 추가 옵션 없이 사용되지만, 다음과 같은 옵션이 있습니다:

- `--help`: 사용법 정보를 표시합니다.
- `--version`: 버전 정보를 표시합니다.

## Common Examples
다음은 `whoami` 명령어의 몇 가지 실용적인 예입니다:

1. 현재 사용자 이름 출력하기:
   ```bash
   whoami
   ```

2. 도움말 정보 보기:
   ```bash
   whoami --help
   ```

3. 버전 정보 확인하기:
   ```bash
   whoami --version
   ```

## Tips
- `whoami`는 스크립트에서 현재 사용자 정보를 확인할 때 유용합니다.
- `whoami`와 `id -un` 명령어는 동일한 결과를 제공합니다. 필요에 따라 선택하여 사용할 수 있습니다.