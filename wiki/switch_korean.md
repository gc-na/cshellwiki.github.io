# [운영 체제] C Shell (csh) switch 사용법: 조건에 따라 명령 실행

## Overview
`switch` 명령은 C Shell에서 조건에 따라 여러 경우를 처리할 수 있는 제어 구조입니다. 주어진 표현식의 값을 평가하여 해당하는 경우에 따라 명령을 실행할 수 있게 해줍니다.

## Usage
기본 구문은 다음과 같습니다:

```
switch (expression)
    case pattern1:
        commands1
        breaksw
    case pattern2:
        commands2
        breaksw
    default:
        default_commands
end
```

## Common Options
- `case pattern:`: 주어진 패턴과 일치하는 경우에 실행할 명령을 정의합니다.
- `breaksw`: 현재 `case` 블록을 종료하고 `switch` 블록을 빠져나갑니다.
- `default:`: 모든 `case` 패턴과 일치하지 않을 때 실행할 기본 명령을 정의합니다.

## Common Examples

### 예제 1: 숫자에 따른 출력
```csh
set num = 2
switch ($num)
    case 1:
        echo "숫자는 1입니다."
        breaksw
    case 2:
        echo "숫자는 2입니다."
        breaksw
    case 3:
        echo "숫자는 3입니다."
        breaksw
    default:
        echo "숫자는 1, 2, 3이 아닙니다."
end
```

### 예제 2: 문자열 패턴 매칭
```csh
set fruit = "사과"
switch ($fruit)
    case "사과":
        echo "과일은 사과입니다."
        breaksw
    case "바나나":
        echo "과일은 바나나입니다."
        breaksw
    default:
        echo "알 수 없는 과일입니다."
end
```

### 예제 3: 여러 패턴 처리
```csh
set color = "파랑"
switch ($color)
    case "빨강":
    case "초록":
    case "파랑":
        echo "색상은 빨강, 초록 또는 파랑입니다."
        breaksw
    default:
        echo "다른 색상입니다."
end
```

## Tips
- `switch`는 표현식의 결과에 따라 여러 경우를 쉽게 처리할 수 있어 코드의 가독성을 높입니다.
- 각 `case` 블록에서 `breaksw`를 사용하여 불필요한 추가 실행을 방지하세요.
- `default` 블록을 사용하여 모든 경우에 대한 예외 처리를 추가하는 것이 좋습니다.