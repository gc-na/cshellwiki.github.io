# [리눅스] Bash sha512sum 사용법: 파일의 SHA-512 해시 생성

## Overview
`sha512sum` 명령어는 파일의 SHA-512 해시 값을 생성하는 데 사용됩니다. 이 해시 값은 파일의 무결성을 확인하거나 파일의 고유성을 검증하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
sha512sum [옵션] [파일]
```

## Common Options
- `-b`, `--binary`: 이진 파일을 처리할 때 사용합니다.
- `-t`, `--text`: 텍스트 파일을 처리할 때 사용합니다.
- `-c`, `--check`: 해시 값을 확인하는 데 사용합니다.
- `--quiet`: 해시 확인 시 오류 메시지만 출력합니다.

## Common Examples
1. **파일의 SHA-512 해시 생성하기**
   ```bash
   sha512sum example.txt
   ```

2. **여러 파일의 SHA-512 해시 생성하기**
   ```bash
   sha512sum file1.txt file2.txt
   ```

3. **해시 값 확인하기**
   해시 값이 저장된 파일을 사용하여 확인할 수 있습니다.
   ```bash
   sha512sum -c hashfile.txt
   ```

4. **이진 파일의 SHA-512 해시 생성하기**
   ```bash
   sha512sum -b binaryfile.bin
   ```

## Tips
- 해시 값을 파일로 저장하려면, 출력 리다이렉션을 사용하세요:
  ```bash
  sha512sum example.txt > example_hash.txt
  ```
- 해시 값을 확인할 때는 항상 원본 파일과 해시 파일이 같은 디렉토리에 있는지 확인하세요.
- 해시 값은 파일의 변경 여부를 감지하는 데 유용하므로, 중요한 파일에 대해 정기적으로 해시를 생성하고 저장하는 것이 좋습니다.