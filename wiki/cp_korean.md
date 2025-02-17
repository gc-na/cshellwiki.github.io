# [리눅스] Bash cp 사용법: 파일 및 디렉토리 복사

## Overview
`cp` 명령어는 파일과 디렉토리를 복사하는 데 사용됩니다. 이 명령어를 통해 원본 파일이나 디렉토리를 다른 위치에 동일하게 복사할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
cp [옵션] [원본] [대상]
```

## Common Options
- `-r`: 디렉토리를 재귀적으로 복사합니다.
- `-i`: 대상 파일이 이미 존재할 경우, 덮어쓰기 전에 사용자에게 확인을 요청합니다.
- `-u`: 원본 파일이 대상 파일보다 최신일 경우에만 복사합니다.
- `-v`: 복사하는 동안 진행 상황을 자세히 보여줍니다.

## Common Examples
- 단일 파일 복사:
    ```bash
    cp file.txt /path/to/destination/
    ```
- 디렉토리 복사 (재귀적):
    ```bash
    cp -r /path/to/source_directory /path/to/destination_directory/
    ```
- 덮어쓰기 확인:
    ```bash
    cp -i file.txt /path/to/destination/
    ```
- 최신 파일만 복사:
    ```bash
    cp -u file.txt /path/to/destination/
    ```
- 진행 상황 표시:
    ```bash
    cp -v file.txt /path/to/destination/
    ```

## Tips
- 항상 중요한 파일을 복사할 때는 `-i` 옵션을 사용하여 실수로 덮어쓰는 것을 방지하세요.
- 대량의 파일을 복사할 때는 `-v` 옵션을 사용하여 복사 진행 상황을 확인하는 것이 유용합니다.
- 디렉토리를 복사할 때는 항상 `-r` 옵션을 잊지 마세요. 그렇지 않으면 오류가 발생합니다.