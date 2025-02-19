# [리눅스] C Shell (csh) foreach 사용법: 반복문 실행

## Overview
`foreach` 명령어는 C Shell에서 반복문을 실행하는 데 사용됩니다. 주어진 리스트의 각 항목에 대해 특정 명령을 반복적으로 실행할 수 있게 해줍니다.

## Usage
기본 문법은 다음과 같습니다:
```
foreach variable (list)
    command
end
```

## Common Options
- `-n`: 명령을 실행하기 전에 각 명령을 출력합니다.
- `-e`: 명령을 실행하기 전에 구문 오류를 검사합니다.

## Common Examples
다음은 `foreach` 명령어의 몇 가지 실용적인 예입니다.

### 예제 1: 숫자 반복
```csh
foreach i (1 2 3 4 5)
    echo $i
end
```
이 코드는 1부터 5까지의 숫자를 출력합니다.

### 예제 2: 파일 목록 처리
```csh
foreach file (*.txt)
    echo "Processing $file"
end
```
현재 디렉토리의 모든 `.txt` 파일을 처리하는 예입니다.

### 예제 3: 문자열 배열 반복
```csh
set colors = (red green blue)
foreach color ($colors)
    echo "Color: $color"
end
```
색상 배열을 반복하여 각 색상을 출력합니다.

## Tips
- `foreach` 문을 사용할 때는 항상 `end`로 블록을 종료해야 합니다.
- 복잡한 명령어를 사용할 때는 명령어를 세미콜론으로 구분하여 한 줄에 작성할 수 있습니다.
- `foreach`는 C Shell 전용이므로 다른 셸에서는 사용할 수 없습니다.