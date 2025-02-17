# [리눅스] Bash gzip 사용법: 파일 압축 및 해제

## Overview
`gzip` 명령어는 파일을 압축하여 저장 공간을 절약하는 데 사용됩니다. 이 명령어는 GNU zip의 약자로, 주로 텍스트 파일을 압축하는 데 효과적입니다. 압축된 파일은 `.gz` 확장자를 가집니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
gzip [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: 압축 해제 모드로 실행합니다.
- `-k`, `--keep`: 원본 파일을 유지하면서 압축합니다.
- `-v`, `--verbose`: 압축 진행 상황을 자세히 출력합니다.
- `-r`, `--recursive`: 디렉토리 내의 모든 파일을 재귀적으로 압축합니다.
- `-f`, `--force`: 기존 파일을 덮어쓰도록 강제합니다.

## Common Examples
- **파일 압축하기**
```bash
gzip example.txt
```
이 명령어는 `example.txt` 파일을 압축하여 `example.txt.gz` 파일을 생성합니다.

- **압축 해제하기**
```bash
gzip -d example.txt.gz
```
이 명령어는 `example.txt.gz` 파일의 압축을 해제하여 원본 파일인 `example.txt`를 복원합니다.

- **원본 파일 유지하면서 압축하기**
```bash
gzip -k example.txt
```
이 명령어는 `example.txt` 파일을 압축하되, 원본 파일을 그대로 유지합니다.

- **디렉토리 내 모든 파일 압축하기**
```bash
gzip -r my_directory/
```
이 명령어는 `my_directory` 내의 모든 파일을 재귀적으로 압축합니다.

## Tips
- 압축된 파일을 쉽게 확인하려면 `ls -lh` 명령어를 사용하여 파일 크기를 비교해 보세요.
- 대량의 파일을 압축할 때는 `-v` 옵션을 사용하여 진행 상황을 모니터링하는 것이 좋습니다.
- 압축 해제 후 원본 파일이 필요 없다면 `gzip -f` 옵션을 사용하여 기존 파일을 덮어쓸 수 있습니다.