# [리눅스] C Shell (csh) endsw 사용법: 조건문 종료

## Overview
`endsw` 명령은 C Shell 스크립트에서 switch 문을 종료하는 데 사용됩니다. 이 명령은 여러 조건을 처리할 때 유용하며, 각 조건에 대한 실행 블록을 정의한 후, 마지막에 `endsw`를 사용하여 switch 문을 마무리합니다.

## Usage
기본 구문은 다음과 같습니다:

```
endsw
```

## Common Options
`endsw` 명령은 옵션을 지원하지 않습니다. 단순히 switch 문을 종료하는 역할만 수행합니다.

## Common Examples
다음은 `endsw` 명령을 사용하는 몇 가지 예입니다.

### 예제 1: 기본적인 switch 문
```csh
set var = "apple"
switch ($var)
    case "apple":
        echo "It's an apple."
        breaksw
    case "banana":
        echo "It's a banana."
        breaksw
    default:
        echo "Unknown fruit."
endsw
```

### 예제 2: 숫자에 대한 switch 문
```csh
set num = 2
switch ($num)
    case 1:
        echo "Number is one."
        breaksw
    case 2:
        echo "Number is two."
        breaksw
    case 3:
        echo "Number is three."
        breaksw
    default:
        echo "Number is not recognized."
endsw
```

### 예제 3: 여러 조건 처리
```csh
set day = "Monday"
switch ($day)
    case "Monday":
        echo "Start of the week."
        breaksw
    case "Friday":
        echo "Almost weekend."
        breaksw
    case "Saturday":
    case "Sunday":
        echo "It's the weekend!"
        breaksw
    default:
        echo "Midweek day."
endsw
```

## Tips
- `endsw`는 반드시 switch 문 블록의 마지막에 위치해야 합니다.
- 각 case 블록에서 `breaksw` 명령을 사용하여 switch 문을 종료할 수 있습니다.
- switch 문을 사용할 때는 변수의 값이 정확히 일치해야 조건이 실행됩니다.