# [리눅스] Bash expand 사용법: 공백을 탭으로 변환

## Overview
`expand` 명령어는 텍스트 파일 내의 공백을 탭으로 변환하는 데 사용됩니다. 이 명령어는 주로 텍스트 파일을 포맷팅할 때 유용하며, 가독성을 높이는 데 도움을 줍니다.

## Usage
기본 구문은 다음과 같습니다:
```
expand [옵션] [인수]
```

## Common Options
- `-t, --tabs=N`: 탭의 너비를 N으로 설정합니다. 기본값은 8입니다.
- `-i, --initial`: 파일의 초기 공백을 탭으로 변환합니다.
- `-n, --no-tabs`: 모든 탭을 유지하고 공백만 변환합니다.

## Common Examples
1. 기본 사용법: 파일의 공백을 탭으로 변환합니다.
   ```bash
   expand input.txt > output.txt
   ```

2. 탭 너비를 4로 설정하여 변환합니다.
   ```bash
   expand -t 4 input.txt > output.txt
   ```

3. 초기 공백만 탭으로 변환합니다.
   ```bash
   expand -i input.txt > output.txt
   ```

4. 공백만 변환하고 탭은 유지합니다.
   ```bash
   expand -n input.txt > output.txt
   ```

## Tips
- 파일을 변환하기 전에 원본 파일을 백업하는 것이 좋습니다.
- `cat` 명령어와 함께 사용하여 변환된 내용을 즉시 확인할 수 있습니다.
  ```bash
  cat output.txt
  ```
- 여러 파일을 한 번에 변환하려면 와일드카드를 사용할 수 있습니다.
  ```bash
  expand *.txt > output.txt
  ```