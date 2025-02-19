# [리눅스] C Shell (csh) if 사용법: 조건에 따라 명령 실행

## Overview
`if` 명령은 조건을 평가하고, 그 결과에 따라 특정 명령을 실행하는 데 사용됩니다. 이는 스크립트 내에서 조건부 로직을 구현하는 데 매우 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```csh
if (조건) then
    명령
endif
```

## Common Options
- `then`: 조건이 참일 때 실행할 명령을 시작하는 키워드입니다.
- `endif`: `if` 블록의 끝을 나타냅니다.

## Common Examples

1. **기본 사용법**:
   ```csh
   set var = 10
   if ($var > 5) then
       echo "변수는 5보다 큽니다."
   endif
   ```

2. **파일 존재 여부 확인**:
   ```csh
   if (-e "파일.txt") then
       echo "파일이 존재합니다."
   else
       echo "파일이 존재하지 않습니다."
   endif
   ```

3. **다중 조건 사용**:
   ```csh
   if ($var < 5) then
       echo "변수는 5보다 작습니다."
   else if ($var == 5) then
       echo "변수는 5입니다."
   else
       echo "변수는 5보다 큽니다."
   endif
   ```

## Tips
- 조건문을 사용할 때는 괄호와 공백에 주의하세요. 올바른 문법이 중요합니다.
- `else`와 `else if`를 사용하여 다양한 조건을 처리할 수 있습니다.
- 스크립트를 작성할 때는 각 조건에 대한 명확한 주석을 추가하여 가독성을 높이세요.