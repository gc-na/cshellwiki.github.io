# [리눅스] Bash case 사용법: 조건에 따라 명령 실행하기

## Overview
`case` 명령은 주어진 패턴에 따라 여러 조건을 검사하고, 해당 조건에 맞는 명령을 실행하는 데 사용됩니다. 이는 복잡한 조건문을 간단하게 처리할 수 있게 해줍니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
case [변수] in
    [패턴1])
        [명령1]
        ;;
    [패턴2])
        [명령2]
        ;;
    *)
        [기본 명령]
        ;;
esac
```

## Common Options
- `*)`: 모든 패턴에 대한 기본 동작을 정의합니다. 주어진 패턴과 일치하지 않을 경우 실행됩니다.

## Common Examples

### 예제 1: 숫자에 따른 메시지 출력
```bash
read -p "숫자를 입력하세요: " num
case $num in
    1)
        echo "하나입니다."
        ;;
    2)
        echo "둘입니다."
        ;;
    3)
        echo "셋입니다."
        ;;
    *)
        echo "1, 2, 3이 아닙니다."
        ;;
esac
```

### 예제 2: 파일 확장자에 따른 처리
```bash
filename="example.txt"
case $filename in
    *.txt)
        echo "텍스트 파일입니다."
        ;;
    *.jpg|*.png)
        echo "이미지 파일입니다."
        ;;
    *)
        echo "알 수 없는 파일 형식입니다."
        ;;
esac
```

### 예제 3: 사용자 입력에 따른 동작
```bash
read -p "원하는 작업을 선택하세요 (start/stop): " action
case $action in
    start)
        echo "시작합니다."
        ;;
    stop)
        echo "중지합니다."
        ;;
    *)
        echo "유효하지 않은 선택입니다."
        ;;
esac
```

## Tips
- `case` 문을 사용할 때는 패턴을 명확하게 정의하여 가독성을 높이세요.
- 여러 패턴을 한 줄에 나열할 수 있어, 코드의 간결성을 유지할 수 있습니다.
- `*)`를 사용하여 기본 동작을 정의함으로써 예외 처리를 쉽게 할 수 있습니다.