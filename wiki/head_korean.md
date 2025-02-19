# [리눅스] C Shell (csh) head 사용법: 파일의 처음 몇 줄을 출력합니다.

## Overview
`head` 명령어는 파일의 처음 몇 줄을 출력하는 데 사용됩니다. 주로 파일의 내용을 빠르게 확인하고자 할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다.
```
head [options] [arguments]
```

## Common Options
- `-n [number]`: 출력할 줄 수를 지정합니다. 기본값은 10줄입니다.
- `-q`: 여러 파일을 처리할 때 파일 이름을 출력하지 않습니다.
- `-v`: 출력하는 파일 이름을 항상 표시합니다.

## Common Examples
- 기본적으로 첫 10줄 출력하기:
    ```csh
    head filename.txt
    ```

- 첫 5줄만 출력하기:
    ```csh
    head -n 5 filename.txt
    ```

- 여러 파일의 첫 10줄 출력하기:
    ```csh
    head file1.txt file2.txt
    ```

- 파일 이름을 출력하지 않고 첫 10줄 출력하기:
    ```csh
    head -q file1.txt file2.txt
    ```

## Tips
- `head` 명령어는 대용량 파일을 다룰 때 유용하며, 파일의 구조나 내용을 빠르게 파악할 수 있도록 도와줍니다.
- `head`와 `tail` 명령어를 함께 사용하면 파일의 처음과 끝 부분을 모두 쉽게 확인할 수 있습니다.
- 스크립트에서 `head`를 사용하여 로그 파일의 최근 내용을 모니터링할 수 있습니다.