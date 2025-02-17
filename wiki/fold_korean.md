# [리눅스] Bash fold 사용법: 텍스트 줄 바꾸기

## Overview
`fold` 명령어는 긴 텍스트 줄을 지정된 너비로 나누어 출력하는 데 사용됩니다. 이 명령어는 주로 텍스트 파일을 읽거나 출력할 때 가독성을 높이기 위해 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
fold [options] [arguments]
```

## Common Options
- `-w, --width=N`: 출력할 최대 너비를 N으로 설정합니다. 기본값은 80입니다.
- `-s, --spaces`: 단어 경계에서 줄을 나누도록 합니다.
- `-b, --bytes`: 바이트 단위로 너비를 설정합니다.

## Common Examples
1. 기본 사용법: 기본 너비로 텍스트 파일을 줄 바꾸기
   ```bash
   fold myfile.txt
   ```

2. 너비를 50자로 설정하여 줄 바꾸기
   ```bash
   fold -w 50 myfile.txt
   ```

3. 단어 경계에서 줄 바꾸기
   ```bash
   fold -s -w 50 myfile.txt
   ```

4. 여러 파일을 동시에 처리하기
   ```bash
   fold file1.txt file2.txt
   ```

## Tips
- `fold` 명령어는 긴 텍스트를 읽기 쉽게 만들기 때문에, 출력 결과를 다른 명령어와 함께 파이프하여 사용할 수 있습니다.
- `man fold` 명령어를 통해 더 많은 옵션과 사용법을 확인할 수 있습니다.
- 스크립트에서 자동화된 보고서를 생성할 때 유용하게 사용할 수 있습니다.