# [리눅스] Bash while 사용법: 반복 실행을 위한 명령어

## Overview
`while` 명령어는 주어진 조건이 참인 동안 특정 명령어를 반복 실행하는 데 사용됩니다. 이 명령어는 주로 스크립트에서 루프를 만들 때 유용하게 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
while [조건]; do
    [명령어]
done
```

## Common Options
`while` 명령어에는 특별한 옵션이 없지만, 조건문에 사용할 수 있는 몇 가지 유용한 테스트 조건이 있습니다:
- `-e`: 파일이 존재하는지 확인합니다.
- `-f`: 파일이 일반 파일인지 확인합니다.
- `-d`: 디렉토리인지 확인합니다.

## Common Examples

### 예제 1: 숫자 카운트
1부터 5까지 숫자를 출력하는 예제입니다.

```bash
count=1
while [ $count -le 5 ]; do
    echo $count
    count=$((count + 1))
done
```

### 예제 2: 파일 존재 확인
특정 파일이 존재하는 동안 메시지를 출력하는 예제입니다.

```bash
filename="test.txt"
while [ -e $filename ]; do
    echo "$filename 파일이 존재합니다."
    sleep 1
done
```

### 예제 3: 사용자 입력 반복
사용자로부터 입력을 받아 "exit"가 입력될 때까지 반복하는 예제입니다.

```bash
input=""
while [ "$input" != "exit" ]; do
    read -p "입력하세요 (exit로 종료): " input
    echo "입력한 내용: $input"
done
```

## Tips
- 조건문을 사용할 때는 항상 조건이 참이 될 수 있는지 확인하세요.
- 무한 루프를 피하기 위해 적절한 종료 조건을 설정하는 것이 중요합니다.
- `sleep` 명령어를 사용하여 루프 실행 간격을 조절할 수 있습니다.