# [리눅스] Bash basename 사용법: 파일 경로에서 파일 이름 추출

## Overview
`basename` 명령어는 주어진 파일 경로에서 파일 이름만 추출하는 데 사용됩니다. 이 명령어는 파일 경로에서 디렉토리 부분을 제거하고, 파일 이름만 반환합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
basename [options] [arguments]
```

## Common Options
- `-a`, `--multiple`: 여러 개의 인수를 처리하여 각 인수에 대해 basename을 반환합니다.
- `-s`, `--suffix`: 지정한 접미사를 제거하고 파일 이름을 반환합니다.

## Common Examples
다음은 `basename` 명령어의 몇 가지 실용적인 예입니다.

1. 기본 사용법:
   ```bash
   basename /usr/local/bin/script.sh
   ```
   출력:
   ```
   script.sh
   ```

2. 접미사 제거:
   ```bash
   basename /usr/local/bin/script.sh .sh
   ```
   출력:
   ```
   script
   ```

3. 여러 파일 이름 추출:
   ```bash
   basename -a /usr/local/bin/script.sh /usr/bin/another_script.py
   ```
   출력:
   ```
   script.sh
   another_script.py
   ```

## Tips
- `basename`을 사용할 때, 접미사를 지정하면 파일 이름을 더 깔끔하게 정리할 수 있습니다.
- 스크립트에서 경로를 처리할 때 유용하게 사용할 수 있으며, 다른 명령어와 조합하여 더욱 강력한 기능을 발휘할 수 있습니다.