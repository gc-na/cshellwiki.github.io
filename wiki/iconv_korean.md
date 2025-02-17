# [리눅스] Bash iconv 사용법: 문자 인코딩 변환

## Overview
`iconv` 명령어는 파일이나 표준 입력의 문자 인코딩을 변환하는 데 사용됩니다. 다양한 문자 인코딩 형식을 지원하여, 데이터의 호환성을 높이고, 다른 시스템 간의 문자 인코딩 문제를 해결할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
iconv [options] [arguments]
```

## Common Options
- `-f, --from-code=CODE`: 변환할 원본 문자 인코딩을 지정합니다.
- `-t, --to-code=CODE`: 변환할 대상 문자 인코딩을 지정합니다.
- `-o, --output=FILE`: 변환된 내용을 저장할 파일을 지정합니다.
- `-c`: 변환할 수 없는 문자들을 무시합니다.
- `-s`: 경고 메시지를 표시하지 않습니다.

## Common Examples
1. UTF-8에서 ISO-8859-1로 변환하기:
    ```bash
    iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
    ```

2. 파일의 문자 인코딩을 확인하고 변환하기:
    ```bash
    iconv -f UTF-16 -t UTF-8 input.txt -o output.txt
    ```

3. 표준 입력을 사용하여 변환하기:
    ```bash
    echo "안녕하세요" | iconv -f UTF-8 -t EUC-KR
    ```

4. 변환할 수 없는 문자를 무시하고 변환하기:
    ```bash
    iconv -f UTF-8 -t ASCII//IGNORE input.txt -o output.txt
    ```

## Tips
- 변환할 파일의 인코딩을 미리 확인하고 사용하는 것이 좋습니다.
- `iconv` 명령어를 사용할 때, 변환할 인코딩이 지원되는지 확인하세요.
- 대량의 파일을 변환할 경우, 스크립트를 작성하여 자동화하는 것이 유용합니다.