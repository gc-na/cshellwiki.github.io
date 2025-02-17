# [리눅스] Bash test 사용법: 조건 평가

## Overview
`test` 명령어는 주어진 조건을 평가하고 그 결과에 따라 참(true) 또는 거짓(false)을 반환합니다. 주로 스크립트에서 조건문을 작성할 때 유용하게 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```
test [options] [arguments]
```

## Common Options
- `-e FILE`: 파일이 존재하는지 확인합니다.
- `-d FILE`: 주어진 경로가 디렉토리인지 확인합니다.
- `-f FILE`: 주어진 경로가 일반 파일인지 확인합니다.
- `-z STRING`: 문자열이 비어 있는지 확인합니다.
- `-n STRING`: 문자열이 비어 있지 않은지 확인합니다.
- `=`: 두 문자열이 같은지 비교합니다.
- `!=`: 두 문자열이 다른지 비교합니다.

## Common Examples
1. 파일 존재 여부 확인:
   ```bash
   test -e /path/to/file && echo "파일이 존재합니다."
   ```

2. 디렉토리 확인:
   ```bash
   test -d /path/to/directory && echo "디렉토리가 존재합니다."
   ```

3. 문자열 비어 있는지 확인:
   ```bash
   STRING=""
   test -z "$STRING" && echo "문자열이 비어 있습니다."
   ```

4. 두 문자열 비교:
   ```bash
   STRING1="hello"
   STRING2="world"
   test "$STRING1" != "$STRING2" && echo "문자열이 다릅니다."
   ```

## Tips
- `test` 명령어는 `[ ]` 구문으로도 사용할 수 있습니다. 예를 들어, `test -e file`는 `[ -e file ]`와 동일합니다.
- 조건문을 사용할 때는 `&&` 또는 `||`를 활용하여 여러 조건을 조합할 수 있습니다.
- 스크립트에서 `test`를 사용할 때는 항상 조건을 명확히 하고, 필요한 경우 에러 메시지를 추가하여 디버깅을 용이하게 하세요.