# [리눅스] Bash break 사용법: 루프 종료

## Overview
`break` 명령어는 Bash 스크립트에서 루프를 종료하는 데 사용됩니다. 주로 `for`, `while`, `until` 루프와 함께 사용되며, 특정 조건이 충족되었을 때 루프의 실행을 중단할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
break [n]
```
여기서 `n`은 종료할 루프의 레벨을 지정합니다. 기본값은 1로, 가장 가까운 루프를 종료합니다.

## Common Options
- `n`: 종료할 루프의 레벨을 지정합니다. 기본값은 1입니다.

## Common Examples

### 예제 1: 기본 사용법
가장 간단한 형태로, `for` 루프에서 `break`를 사용하여 루프를 종료합니다.
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo $i
done
```
이 코드는 1과 2를 출력하고, 3에서 루프를 종료합니다.

### 예제 2: 중첩 루프에서의 사용
중첩된 루프에서 특정 레벨의 루프를 종료할 수 있습니다.
```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      break 2
    fi
    echo "$i, $j"
  done
done
```
이 코드는 1, 1과 1, 2를 출력한 후 두 개의 루프를 모두 종료합니다.

### 예제 3: 조건부 종료
조건에 따라 루프를 종료하는 예제입니다.
```bash
count=0
while true; do
  count=$((count + 1))
  if [ $count -ge 5 ]; then
    break
  fi
  echo "Count is $count"
done
```
이 코드는 1부터 5까지의 카운트를 출력하고, 5에 도달했을 때 루프를 종료합니다.

## Tips
- `break`를 사용할 때는 종료 조건을 명확히 설정하여 예기치 않은 종료를 방지하세요.
- 중첩 루프에서 `break n`을 사용하여 특정 레벨의 루프만 종료할 수 있으므로, 복잡한 루프 구조에서 유용합니다.
- 디버깅 시, `echo` 명령어와 함께 사용하여 루프의 흐름을 확인하는 것이 좋습니다.