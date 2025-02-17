# [리눅스] Bash xargs 사용법: 명령어의 출력을 인수로 변환

## Overview
`xargs` 명령어는 표준 입력으로부터 데이터를 읽어 다른 명령어의 인수로 변환하는 도구입니다. 이를 통해 긴 인수 목록을 처리하거나 여러 개의 파일을 한 번에 다룰 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
xargs [options] [arguments]
```

## Common Options
- `-n N`: 각 호출에서 N개의 인수만 사용합니다.
- `-d DELIM`: 입력 구분자를 DELIM으로 설정합니다.
- `-p`: 각 명령 실행 전에 사용자에게 확인을 요청합니다.
- `-0`: 널 문자로 구분된 입력을 처리합니다. 주로 `find`와 함께 사용됩니다.

## Common Examples
1. **파일 목록을 삭제하기:**
   ```bash
   find . -name "*.tmp" | xargs rm
   ```
   위 명령어는 현재 디렉토리에서 `.tmp` 파일을 찾아 삭제합니다.

2. **파일 내용 검색하기:**
   ```bash
   find . -name "*.txt" | xargs grep "검색어"
   ```
   현재 디렉토리의 모든 `.txt` 파일에서 "검색어"를 검색합니다.

3. **명령어에 인수 전달하기:**
   ```bash
   echo "file1 file2 file3" | xargs -n 1 cp -v /source/directory/
   ```
   `file1`, `file2`, `file3`를 `/source/directory/`로 복사합니다. 각 파일을 개별적으로 처리합니다.

4. **널 문자로 구분된 파일 처리하기:**
   ```bash
   find . -name "*.jpg" -print0 | xargs -0 mv -t /destination/directory/
   ```
   널 문자로 구분된 `.jpg` 파일을 `/destination/directory/`로 이동합니다.

## Tips
- `xargs`를 사용할 때는 인수의 길이가 시스템의 제한을 초과하지 않도록 주의하세요.
- `-n` 옵션을 활용하여 한 번에 처리할 인수의 수를 조절하면 메모리 사용을 최적화할 수 있습니다.
- `-0` 옵션과 함께 `find` 명령어를 사용하면 파일 이름에 공백이 포함된 경우에도 안전하게 처리할 수 있습니다.