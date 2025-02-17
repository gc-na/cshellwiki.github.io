# [리눅스] Bash switch 사용법: 명령어의 조건을 전환합니다.

## Overview
`switch` 명령어는 주어진 조건에 따라 여러 가지 경로 중 하나를 선택하는 데 사용됩니다. 주로 스크립트 내에서 조건 분기를 처리할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
switch [options] [arguments]
```

## Common Options
- `-c` : 특정 조건에 대한 경우를 지정합니다.
- `-d` : 기본값을 설정합니다.
- `-h` : 도움말을 표시합니다.

## Common Examples
다음은 `switch` 명령어의 몇 가지 실용적인 예입니다.

### 예제 1: 기본적인 switch 사용
```bash
case $variable in
    "value1")
        echo "Value is 1"
        ;;
    "value2")
        echo "Value is 2"
        ;;
    *)
        echo "Default value"
        ;;
esac
```

### 예제 2: 여러 조건 처리
```bash
case $day in
    "Monday")
        echo "Start of the week"
        ;;
    "Friday")
        echo "End of the week"
        ;;
    *)
        echo "Midweek"
        ;;
esac
```

### 예제 3: 사용자 입력에 따른 분기
```bash
read -p "Enter a number (1-3): " number
case $number in
    1)
        echo "You chose one."
        ;;
    2)
        echo "You chose two."
        ;;
    3)
        echo "You chose three."
        ;;
    *)
        echo "Invalid choice."
        ;;
esac
```

## Tips
- `switch` 명령어를 사용할 때는 항상 기본값을 설정하여 예기치 않은 입력에 대한 처리를 준비하세요.
- 조건을 명확하게 작성하여 가독성을 높이고 유지보수를 쉽게 하세요.
- 여러 조건을 처리할 때는 가능한 한 간결하게 작성하여 코드의 복잡성을 줄이세요.