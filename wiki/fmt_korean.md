# [리눅스] C Shell (csh) fmt 사용법: 텍스트 포맷팅

## Overview
`fmt` 명령어는 텍스트 파일의 줄 길이를 조정하여 가독성을 높이는 데 사용됩니다. 이 명령어는 긴 문장을 적절한 길이로 나누어 출력합니다.

## Usage
기본 구문은 다음과 같습니다:
```
fmt [options] [arguments]
```

## Common Options
- `-w <width>`: 출력할 최대 줄 길이를 설정합니다. 기본값은 75자입니다.
- `-s`: 공백 줄을 유지합니다. 연속된 공백 줄이 하나로 합쳐지지 않도록 합니다.
- `-u`: 줄을 정렬하지 않고, 원래의 형식을 유지합니다.

## Common Examples
1. 기본 사용법: 텍스트 파일의 줄 길이를 자동으로 조정합니다.
   ```bash
   fmt example.txt
   ```

2. 최대 줄 길이를 50자로 설정합니다.
   ```bash
   fmt -w 50 example.txt
   ```

3. 공백 줄을 유지하면서 포맷팅합니다.
   ```bash
   fmt -s example.txt
   ```

4. 여러 파일을 동시에 포맷팅합니다.
   ```bash
   fmt file1.txt file2.txt
   ```

## Tips
- 긴 문장을 다루는 경우, 적절한 줄 길이를 설정하여 가독성을 높이는 것이 좋습니다.
- `-s` 옵션을 사용하여 공백 줄을 유지하면 문서의 구조를 보존할 수 있습니다.
- 포맷팅된 결과를 새로운 파일에 저장하려면 리다이렉션을 사용할 수 있습니다:
  ```bash
  fmt example.txt > formatted_example.txt
  ```