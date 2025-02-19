# [리눅스] C Shell (csh) bunzip2 사용법: bzip2 압축 해제

## Overview
`bunzip2` 명령어는 bzip2 형식으로 압축된 파일을 해제하는 데 사용됩니다. 이 명령어는 파일의 크기를 줄이기 위해 bzip2 알고리즘을 사용하여 압축된 데이터를 원래 상태로 복원합니다.

## Usage
기본 구문은 다음과 같습니다:
```
bunzip2 [options] [arguments]
```

## Common Options
- `-k`: 압축 해제 후 원본 파일을 삭제하지 않고 유지합니다.
- `-f`: 강제로 압축 해제를 수행합니다. 이미 존재하는 파일이 있을 경우 덮어씁니다.
- `-v`: 압축 해제 과정에서 자세한 정보를 출력합니다.

## Common Examples
1. 기본 압축 해제:
   ```bash
   bunzip2 example.bz2
   ```

2. 원본 파일 유지하면서 압축 해제:
   ```bash
   bunzip2 -k example.bz2
   ```

3. 강제로 압축 해제:
   ```bash
   bunzip2 -f example.bz2
   ```

4. 압축 해제 과정의 자세한 정보 출력:
   ```bash
   bunzip2 -v example.bz2
   ```

## Tips
- 압축 해제 후 원본 파일을 유지하고 싶다면 `-k` 옵션을 사용하는 것이 좋습니다.
- 이미 존재하는 파일이 있을 경우, `-f` 옵션을 사용하여 덮어쓸 수 있습니다.
- 압축 해제 진행 상황을 확인하고 싶다면 `-v` 옵션을 활용하세요.