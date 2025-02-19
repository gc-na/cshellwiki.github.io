# [리눅스] C Shell (csh) bzip2 사용법: 파일 압축 및 해제

## Overview
bzip2 명령어는 파일을 압축하고 해제하는 데 사용됩니다. 이 명령어는 특히 대용량 파일을 효율적으로 압축하는 데 유용하며, 높은 압축률을 제공합니다.

## Usage
기본적인 bzip2 명령어 구문은 다음과 같습니다.

```bash
bzip2 [옵션] [인수]
```

## Common Options
- `-d`, `--decompress`: 압축 해제 모드로 실행합니다.
- `-k`, `--keep`: 원본 파일을 유지하면서 압축합니다.
- `-f`, `--force`: 기존 파일을 덮어쓰도록 강제합니다.
- `-v`, `--verbose`: 압축 진행 상황을 자세히 출력합니다.

## Common Examples
- 파일 압축하기:
```bash
bzip2 example.txt
```

- 압축 해제하기:
```bash
bzip2 -d example.txt.bz2
```

- 원본 파일 유지하면서 압축하기:
```bash
bzip2 -k example.txt
```

- 압축 진행 상황 확인하기:
```bash
bzip2 -v example.txt
```

## Tips
- 대용량 파일을 압축할 때 bzip2를 사용하면 저장 공간을 절약할 수 있습니다.
- 압축된 파일은 `.bz2` 확장자를 가지므로, 파일 형식을 쉽게 식별할 수 있습니다.
- bzip2는 다른 압축 도구보다 느릴 수 있지만, 압축률이 높기 때문에 중요한 파일에 적합합니다.