# [리눅스] Bash printenv 사용법: 환경 변수 출력

## Overview
`printenv` 명령어는 현재 세션의 환경 변수를 출력하는 데 사용됩니다. 이 명령어를 통해 시스템에서 설정된 환경 변수의 값을 쉽게 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
printenv [options] [arguments]
```

## Common Options
- `-0`, `--null`: 출력 결과를 널 문자로 구분합니다.
- `NAME`: 특정 환경 변수의 값을 출력합니다. 변수 이름을 인자로 제공하면 해당 변수의 값만 표시됩니다.

## Common Examples
1. 모든 환경 변수 출력하기:
   ```bash
   printenv
   ```

2. 특정 환경 변수 출력하기 (예: `HOME` 변수):
   ```bash
   printenv HOME
   ```

3. 널 문자로 구분된 환경 변수 출력하기:
   ```bash
   printenv -0
   ```

## Tips
- `printenv`는 `env` 명령어와 유사하지만, 특정 변수의 값을 직접 확인할 수 있는 점에서 유용합니다.
- 스크립트에서 환경 변수를 확인하고자 할 때 유용하게 사용할 수 있습니다.
- 환경 변수가 설정되어 있지 않은 경우, 아무 것도 출력되지 않으니 주의하세요.