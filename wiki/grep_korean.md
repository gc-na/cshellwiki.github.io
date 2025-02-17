# [리눅스] Bash grep 사용법: 텍스트에서 패턴 검색

## Overview
`grep` 명령어는 파일이나 입력 스트림에서 특정 패턴을 검색하는 데 사용됩니다. 이 명령어는 주로 텍스트 파일에서 원하는 문자열을 찾는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
grep [options] [arguments]
```

## Common Options
- `-i`: 대소문자를 구분하지 않고 검색합니다.
- `-v`: 패턴과 일치하지 않는 행을 출력합니다.
- `-r`: 하위 디렉토리를 포함하여 재귀적으로 검색합니다.
- `-n`: 일치하는 행의 번호를 함께 출력합니다.
- `-l`: 패턴이 포함된 파일 이름만 출력합니다.

## Common Examples
1. 특정 문자열 검색:
   ```bash
   grep "hello" file.txt
   ```

2. 대소문자 구분 없이 검색:
   ```bash
   grep -i "hello" file.txt
   ```

3. 패턴이 포함되지 않은 행 출력:
   ```bash
   grep -v "hello" file.txt
   ```

4. 재귀적으로 디렉토리 내 모든 파일에서 검색:
   ```bash
   grep -r "hello" /path/to/directory
   ```

5. 일치하는 행의 번호와 함께 출력:
   ```bash
   grep -n "hello" file.txt
   ```

6. 패턴이 포함된 파일 이름만 출력:
   ```bash
   grep -l "hello" *.txt
   ```

## Tips
- 여러 패턴을 동시에 검색하려면 `-e` 옵션을 사용하세요.
- 정규 표현식을 활용하여 더 복잡한 패턴을 검색할 수 있습니다.
- 파이프(`|`)와 함께 사용하여 다른 명령어의 출력을 필터링할 수 있습니다.