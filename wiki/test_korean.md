# [리눅스] C Shell (csh) test 사용법: 조건 평가

## Overview
`test` 명령은 조건을 평가하는 데 사용됩니다. 이 명령은 주로 스크립트에서 조건문을 작성할 때 유용하며, 파일의 존재 여부나 변수의 값 등을 확인하는 데 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```csh
test [options] [arguments]
```

## Common Options
- `-e FILE`: 지정한 파일이 존재하는지 확인합니다.
- `-d FILE`: 지정한 파일이 디렉토리인지 확인합니다.
- `-f FILE`: 지정한 파일이 일반 파일인지 확인합니다.
- `-z STRING`: 문자열의 길이가 0인지 확인합니다.
- `-n STRING`: 문자열의 길이가 0이 아닌지 확인합니다.
- `STRING1 = STRING2`: 두 문자열이 같은지 비교합니다.

## Common Examples
- 파일 존재 여부 확인:
```csh
if ( `test -e myfile.txt` ) then
    echo "파일이 존재합니다."
else
    echo "파일이 존재하지 않습니다."
endif
```

- 디렉토리 확인:
```csh
if ( `test -d mydir` ) then
    echo "디렉토리가 존재합니다."
else
    echo "디렉토리가 존재하지 않습니다."
endif
```

- 문자열 길이 확인:
```csh
set mystring = ""
if ( `test -z "$mystring"` ) then
    echo "문자열이 비어 있습니다."
endif
```

- 두 문자열 비교:
```csh
set str1 = "hello"
set str2 = "world"
if ( `test "$str1" = "$str2"` ) then
    echo "문자열이 같습니다."
else
    echo "문자열이 다릅니다."
endif
```

## Tips
- `test` 명령은 `[`와 `]`로 대체할 수 있습니다. 예를 들어, `test -e myfile.txt`는 `[ -e myfile.txt ]`와 동일합니다.
- 조건문을 사용할 때는 항상 `then`과 `endif`를 명시적으로 작성하여 가독성을 높이세요.
- 복잡한 조건을 사용할 때는 괄호를 사용하여 우선순위를 명확히 하세요.