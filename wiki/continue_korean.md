# [리눅스] Bash continue 사용법: 루프를 계속 진행하기

## Overview
`continue` 명령은 Bash 스크립트 내에서 루프를 제어하는 데 사용됩니다. 이 명령은 현재 반복을 중단하고 다음 반복으로 넘어가게 합니다. 주로 조건문과 함께 사용되어 특정 조건을 만족할 때만 루프의 나머지 부분을 건너뛰고 다음 반복을 실행하도록 합니다.

## Usage
기본 구문은 다음과 같습니다:
```
continue [options]
```

## Common Options
- `n`: 특정 반복에서 몇 번째 반복을 건너뛸지를 지정합니다. 예를 들어, `continue 2`는 두 번째 다음 반복으로 넘어갑니다.

## Common Examples

### 예제 1: 기본 사용법
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    continue
  fi
  echo $i
done
```
이 스크립트는 1부터 5까지의 숫자를 출력하지만, 3은 건너뜁니다.

### 예제 2: 조건문과 함께 사용
```bash
for i in {1..10}; do
  if [ $((i % 2)) -eq 0 ]; then
    continue
  fi
  echo $i
done
```
이 스크립트는 홀수만 출력합니다. 짝수일 경우 `continue` 명령으로 다음 반복으로 넘어갑니다.

### 예제 3: 중첩 루프에서 사용
```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      continue
    fi
    echo "i: $i, j: $j"
  done
done
```
이 스크립트는 중첩 루프에서 `j`가 2일 때 해당 반복을 건너뛰고 출력합니다.

## Tips
- `continue` 명령은 주로 `for`, `while`, `until` 루프와 함께 사용됩니다.
- 루프의 흐름을 명확하게 이해하고 사용해야 합니다. 조건문을 적절히 설정하여 의도한 대로 루프가 작동하도록 하세요.
- 디버깅 시, `echo` 명령을 사용하여 현재 반복의 상태를 출력하면 `continue`의 동작을 이해하는 데 도움이 됩니다.