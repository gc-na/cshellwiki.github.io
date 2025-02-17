# [리눅스] Bash xz 사용법: 파일 압축 및 해제

## Overview
`xz` 명령어는 파일을 압축하고 해제하는 데 사용됩니다. 이 명령어는 높은 압축률을 제공하며, 주로 대용량 파일을 효율적으로 저장할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
xz [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: 압축 해제 모드로 실행합니다.
- `-k`, `--keep`: 원본 파일을 삭제하지 않고 압축합니다.
- `-f`, `--force`: 기존 파일을 덮어쓰도록 강제합니다.
- `-z`, `--compress`: 압축 모드로 실행합니다 (기본값).
- `-v`, `--verbose`: 압축 또는 해제 과정의 자세한 정보를 출력합니다.

## Common Examples
- 파일 압축하기:
  ```bash
  xz example.txt
  ```
  이 명령어는 `example.txt` 파일을 압축하여 `example.txt.xz`로 저장합니다.

- 압축 해제하기:
  ```bash
  xz -d example.txt.xz
  ```
  이 명령어는 `example.txt.xz` 파일을 해제하여 원본 파일인 `example.txt`를 복원합니다.

- 원본 파일 유지하면서 압축하기:
  ```bash
  xz -k example.txt
  ```
  이 명령어는 `example.txt` 파일을 압축하되, 원본 파일을 삭제하지 않습니다.

- 압축 해제 시 덮어쓰기 강제하기:
  ```bash
  xz -f -d example.txt.xz
  ```
  이 명령어는 기존의 `example.txt` 파일을 덮어쓰면서 압축을 해제합니다.

## Tips
- 대용량 파일을 압축할 때는 `-k` 옵션을 사용하여 원본 파일을 유지하는 것이 좋습니다.
- `-v` 옵션을 사용하면 압축 진행 상황을 확인할 수 있어 유용합니다.
- 여러 파일을 한 번에 압축하려면 와일드카드(`*`)를 사용할 수 있습니다. 예를 들어, `xz *.txt`는 모든 `.txt` 파일을 압축합니다.