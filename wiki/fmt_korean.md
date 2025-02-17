# [리눅스] Bash fmt 사용법: 텍스트 포맷팅

## Overview
`fmt` 명령어는 텍스트 파일의 줄 길이를 조정하여 포맷팅하는 데 사용됩니다. 주로 문서의 가독성을 높이기 위해 긴 줄을 적절한 길이로 나누는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
fmt [options] [arguments]
```

## Common Options
- `-w, --width=N`: 출력할 최대 줄 길이를 N으로 설정합니다. 기본값은 75입니다.
- `-s, --split-only`: 줄을 나누기만 하고, 공백을 추가하지 않습니다.
- `-p, --paragraphs`: 단락을 구분하여 포맷팅합니다.

## Common Examples
1. 기본 사용법: 텍스트 파일 포맷팅
   ```bash
   fmt example.txt
   ```

2. 최대 줄 길이를 50으로 설정하여 포맷팅
   ```bash
   fmt -w 50 example.txt
   ```

3. 공백을 추가하지 않고 줄 나누기
   ```bash
   fmt -s example.txt
   ```

4. 여러 파일 포맷팅
   ```bash
   fmt file1.txt file2.txt
   ```

## Tips
- `fmt` 명령어는 기본적으로 표준 입력을 사용하므로, 파이프와 함께 사용하여 다른 명령어의 출력을 포맷팅할 수 있습니다.
- 포맷팅된 내용을 새로운 파일로 저장하려면 리다이렉션을 사용할 수 있습니다:
  ```bash
  fmt example.txt > formatted_example.txt
  ```
- 긴 문서의 경우, `-p` 옵션을 사용하여 단락을 구분하면 더 깔끔한 결과를 얻을 수 있습니다.