# [리눅스] Bash bzip2 사용법: 파일 압축 및 해제

## Overview
bzip2 명령어는 파일을 압축하는 데 사용되는 도구로, 높은 압축률을 자랑합니다. 주로 대용량 파일을 효율적으로 저장하거나 전송할 때 유용합니다.

## Usage
bzip2의 기본 구문은 다음과 같습니다.

```
bzip2 [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: 압축 해제 모드로 실행합니다.
- `-k`, `--keep`: 원본 파일을 유지하면서 압축합니다.
- `-f`, `--force`: 기존 파일을 덮어쓰도록 강제합니다.
- `-v`, `--verbose`: 압축 진행 상황을 자세히 출력합니다.

## Common Examples
- **파일 압축하기**:
  ```bash
  bzip2 example.txt
  ```
  위 명령어는 `example.txt` 파일을 압축하여 `example.txt.bz2` 파일을 생성합니다.

- **압축 해제하기**:
  ```bash
  bzip2 -d example.txt.bz2
  ```
  이 명령어는 `example.txt.bz2` 파일의 압축을 해제하여 원본 파일인 `example.txt`를 복원합니다.

- **원본 파일 유지하면서 압축하기**:
  ```bash
  bzip2 -k example.txt
  ```
  이 명령어는 `example.txt` 파일을 압축하되, 원본 파일을 그대로 유지합니다.

- **압축 진행 상황 보기**:
  ```bash
  bzip2 -v example.txt
  ```
  이 명령어는 압축 진행 상황을 자세히 출력하면서 `example.txt`를 압축합니다.

## Tips
- 대용량 파일을 압축할 때는 `-k` 옵션을 사용하여 원본 파일을 보존하는 것이 좋습니다.
- 여러 파일을 한 번에 압축하려면 `tar` 명령어와 함께 사용하는 것이 효율적입니다.
- 압축된 파일의 용량을 줄이려면 `bzip2` 대신 `pbzip2`를 사용해 멀티코어 CPU를 활용할 수 있습니다.