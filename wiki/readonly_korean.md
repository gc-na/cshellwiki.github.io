# [리눅스] Bash readonly 사용법: 변수의 읽기 전용 설정

## Overview
`readonly` 명령어는 Bash에서 변수를 읽기 전용으로 설정하는 데 사용됩니다. 이 명령어를 통해 설정된 변수는 이후에 값을 변경할 수 없게 되어, 스크립트나 세션에서 중요한 값을 보호하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
readonly [options] [arguments]
```

## Common Options
- `-p`: 현재 읽기 전용 변수 목록을 출력합니다.

## Common Examples

1. **변수 읽기 전용 설정하기**
   ```bash
   myVar="Hello, World!"
   readonly myVar
   ```

2. **읽기 전용 변수 변경 시도하기**
   ```bash
   myVar="Hello, World!"
   readonly myVar
   myVar="New Value"  # 오류 발생: readonly 변수 변경 불가
   ```

3. **읽기 전용 변수 목록 출력하기**
   ```bash
   readonly -p
   ```

## Tips
- 읽기 전용 변수를 설정할 때는 해당 변수가 정말로 변경되지 않아야 하는지 확인하세요.
- 스크립트의 중요한 설정값이나 환경 변수를 보호하기 위해 `readonly`를 활용하세요.
- `readonly`로 설정된 변수를 해제할 수 없으므로, 필요할 경우 변수를 재정의하기 전에 주의해야 합니다.