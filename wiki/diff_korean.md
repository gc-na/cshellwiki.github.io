# [리눅스] Bash diff 사용법: 파일 간의 차이점 비교

## Overview
`diff` 명령어는 두 파일 간의 차이점을 비교하여 어떤 부분이 다른지를 보여주는 유용한 도구입니다. 주로 소스 코드나 텍스트 파일의 변경 사항을 확인할 때 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
diff [options] [file1] [file2]
```

## Common Options
- `-u`: 유니파이드 형식으로 출력하여 변경된 내용을 더 쉽게 읽을 수 있도록 합니다.
- `-i`: 대소문자를 무시하고 비교합니다.
- `-w`: 공백을 무시하고 비교합니다.
- `-r`: 디렉토리 내의 모든 파일을 재귀적으로 비교합니다.

## Common Examples
1. 두 텍스트 파일 비교:
   ```bash
   diff file1.txt file2.txt
   ```

2. 유니파이드 형식으로 출력:
   ```bash
   diff -u file1.txt file2.txt
   ```

3. 대소문자를 무시하고 비교:
   ```bash
   diff -i file1.txt file2.txt
   ```

4. 두 디렉토리의 파일 비교:
   ```bash
   diff -r dir1/ dir2/
   ```

## Tips
- 변경 사항을 쉽게 이해하려면 `-u` 옵션을 사용하는 것이 좋습니다.
- 파일의 내용이 많을 경우 `less`와 함께 파이프하여 결과를 페이지 단위로 확인할 수 있습니다:
  ```bash
  diff file1.txt file2.txt | less
  ```
- 스크립트에서 `diff`의 결과를 활용하여 자동화된 테스트를 수행할 수 있습니다.