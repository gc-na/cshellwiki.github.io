# [리눅스] Bash endif 사용법: 조건문 종료

## Overview
`endif` 명령어는 Bash 스크립트에서 조건문을 종료하는 데 사용됩니다. 이는 `if` 문과 함께 사용되어 조건이 끝났음을 나타냅니다. `endif`는 주로 `if` 문과 `then` 블록을 명확하게 구분하는 데 도움을 줍니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
endif
```

## Common Options
`endif` 명령어는 별도의 옵션을 가지지 않습니다. 이는 단순히 조건문을 종료하는 역할을 합니다.

## Common Examples
다음은 `endif`를 사용하는 몇 가지 예시입니다.

### 예제 1: 기본 if 문
```bash
if [ "$VAR" -eq 1 ]; then
    echo "VAR는 1입니다."
endif
```

### 예제 2: 여러 조건문
```bash
if [ "$VAR" -eq 1 ]; then
    echo "VAR는 1입니다."
elif [ "$VAR" -eq 2 ]; then
    echo "VAR는 2입니다."
endif
```

### 예제 3: 중첩 if 문
```bash
if [ "$VAR" -eq 1 ]; then
    echo "VAR는 1입니다."
    if [ "$ANOTHER_VAR" -eq 5 ]; then
        echo "ANOTHER_VAR는 5입니다."
    endif
endif
```

## Tips
- `endif`는 Bash에서 기본적으로 지원되지 않으며, `fi`를 사용해야 합니다. 따라서 `if` 문을 종료할 때는 `fi`를 사용하세요.
- 조건문을 작성할 때는 항상 들여쓰기를 통해 가독성을 높이는 것이 좋습니다.
- 복잡한 조건문을 사용할 때는 주석을 추가하여 코드의 이해를 돕는 것이 유용합니다.