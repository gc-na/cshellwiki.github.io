# [리눅스] C Shell (csh) basename 사용법: 파일 경로에서 파일 이름 추출

## Overview
`basename` 명령은 주어진 파일 경로에서 파일 이름만 추출하는 데 사용됩니다. 이 명령은 파일 경로에서 디렉토리 부분을 제거하고 순수한 파일 이름을 반환합니다.

## Usage
기본 구문은 다음과 같습니다:

```
basename [options] [arguments]
```

## Common Options
- `-a`: 여러 파일 경로를 한 번에 처리합니다.
- `-s`: 지정된 접두사 또는 접미사를 제거합니다.

## Common Examples
다음은 `basename` 명령의 몇 가지 실용적인 예입니다.

1. 기본 사용법:
   ```csh
   basename /usr/local/bin/script.sh
   ```
   출력: `script.sh`

2. 접미사 제거:
   ```csh
   basename /usr/local/bin/script.sh .sh
   ```
   출력: `script`

3. 여러 파일 경로 처리:
   ```csh
   basename -a /usr/local/bin/script.sh /usr/bin/another_script.py
   ```
   출력:
   ```
   script.sh
   another_script.py
   ```

## Tips
- `basename` 명령은 스크립트에서 파일 이름을 동적으로 처리할 때 유용합니다.
- 접미사를 제거할 때는 정확한 접미사를 지정해야 원하는 결과를 얻을 수 있습니다.
- 여러 파일을 처리할 때는 `-a` 옵션을 사용하여 한 번에 여러 파일 이름을 추출할 수 있습니다.