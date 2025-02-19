# [리눅스] C Shell (csh) break 사용법: 루프 종료

## Overview
`break` 명령은 C Shell 스크립트에서 루프를 종료하는 데 사용됩니다. 이 명령은 반복문 안에서 특정 조건이 충족되었을 때 루프를 빠져나오고자 할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
break [options]
```

## Common Options
`break` 명령은 일반적으로 옵션을 사용하지 않지만, 특정 상황에서 루프의 깊이를 지정할 수 있습니다. 

- `n`: 종료할 루프의 깊이를 지정합니다. 기본값은 1입니다.

## Common Examples

### 예제 1: 기본 사용
```csh
foreach i (1 2 3 4 5)
    if ($i == 3) then
        break
    endif
    echo $i
end
```
이 예제에서는 1과 2가 출력되고, 3에서 루프가 종료됩니다.

### 예제 2: 루프 깊이 지정
```csh
set count = 0
while (1)
    @ count++
    if ($count == 2) then
        break 2
    endif
    echo $count
end
```
이 예제에서는 `count`가 1과 2를 출력하고, 루프가 두 번 종료됩니다.

### 예제 3: 중첩 루프에서의 사용
```csh
foreach i (1 2)
    foreach j (1 2 3)
        if ($j == 2) then
            break
        endif
        echo "$i, $j"
    end
end
```
이 예제에서는 `(1, 1)`, `(1, 2)`, `(2, 1)`, `(2, 2)`가 출력됩니다. 내부 루프에서 2가 발견되면 내부 루프가 종료됩니다.

## Tips
- `break` 명령은 루프를 조기에 종료할 수 있는 유용한 도구입니다. 조건문과 함께 사용하여 더욱 효과적으로 활용할 수 있습니다.
- 중첩 루프에서 `break n`을 사용하면 특정 깊이의 루프를 종료할 수 있으므로 복잡한 루프 구조에서도 유용합니다.
- 루프 종료 조건을 명확하게 설정하여 코드의 가독성을 높이는 것이 좋습니다.