# [리눅스] C Shell (csh) sort 사용법: 데이터 정렬

## Overview
`sort` 명령어는 텍스트 파일의 내용을 정렬하는 데 사용됩니다. 이 명령어는 기본적으로 알파벳 순서 또는 숫자 순서로 데이터를 정렬할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```
sort [options] [arguments]
```

## Common Options
- `-n`: 숫자 기준으로 정렬합니다.
- `-r`: 역순으로 정렬합니다.
- `-k`: 특정 필드를 기준으로 정렬합니다.
- `-u`: 중복된 줄을 제거합니다.

## Common Examples
- 기본 알파벳 순서로 정렬하기:
    ```csh
    sort filename.txt
    ```

- 숫자 기준으로 정렬하기:
    ```csh
    sort -n numbers.txt
    ```

- 역순으로 정렬하기:
    ```csh
    sort -r filename.txt
    ```

- 특정 필드를 기준으로 정렬하기 (예: 두 번째 필드):
    ```csh
    sort -k 2 filename.txt
    ```

- 중복된 줄 제거하기:
    ```csh
    sort -u filename.txt
    ```

## Tips
- 정렬할 파일이 클 경우, 결과를 다른 파일로 저장하려면 `-o` 옵션을 사용하세요:
    ```csh
    sort filename.txt -o sorted.txt
    ```
- 여러 옵션을 조합하여 사용할 수 있습니다. 예를 들어, 숫자 기준으로 역순 정렬하려면:
    ```csh
    sort -n -r numbers.txt
    ```
- 정렬된 결과를 화면에 출력하는 대신 파일에 저장하는 것이 좋습니다. 이렇게 하면 나중에 쉽게 참조할 수 있습니다.