# [리눅스] Bash uniq 사용법: 중복된 줄 제거

## Overview
`uniq` 명령어는 텍스트 파일에서 중복된 줄을 제거하는 데 사용됩니다. 이 명령어는 주로 정렬된 파일에서 중복된 항목을 필터링하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
uniq [options] [arguments]
```

## Common Options
- `-c`: 각 줄의 중복 횟수를 함께 출력합니다.
- `-d`: 중복된 줄만 출력합니다.
- `-u`: 중복되지 않은 줄만 출력합니다.
- `-i`: 대소문자를 구분하지 않고 비교합니다.
- `-w N`: 첫 N글자만 비교하여 중복을 판단합니다.

## Common Examples
중복된 줄을 제거하는 기본 예제:
```bash
uniq input.txt output.txt
```

중복된 줄의 개수를 함께 출력하는 예제:
```bash
uniq -c input.txt
```

중복된 줄만 출력하는 예제:
```bash
uniq -d input.txt
```

대소문자를 구분하지 않고 중복을 제거하는 예제:
```bash
uniq -i input.txt output.txt
```

첫 5글자만 비교하여 중복을 제거하는 예제:
```bash
uniq -w 5 input.txt output.txt
```

## Tips
- `uniq` 명령어는 입력 파일이 정렬되어 있어야 제대로 작동합니다. 필요하다면 `sort` 명령어와 함께 사용하세요.
- 중복된 줄을 제거한 후 결과를 새로운 파일에 저장하는 것이 좋습니다.
- `uniq` 명령어는 파이프와 함께 사용하여 다른 명령어의 출력을 필터링하는 데 유용합니다.