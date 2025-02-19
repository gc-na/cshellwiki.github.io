# [리눅스] C Shell (csh) mkdir 사용법: 디렉토리 생성

## Overview
`mkdir` 명령어는 새로운 디렉토리를 생성하는 데 사용됩니다. 이 명령어를 통해 사용자는 원하는 위치에 새로운 폴더를 쉽게 만들 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
mkdir [옵션] [인수]
```

## Common Options
- `-p`: 부모 디렉토리가 없는 경우, 부모 디렉토리도 함께 생성합니다.
- `-m`: 생성할 디렉토리의 권한을 설정합니다.
- `-v`: 생성된 디렉토리에 대한 정보를 출력합니다.

## Common Examples
1. 기본 디렉토리 생성:
   ```csh
   mkdir myfolder
   ```

2. 여러 디렉토리 한 번에 생성:
   ```csh
   mkdir folder1 folder2 folder3
   ```

3. 부모 디렉토리와 함께 생성:
   ```csh
   mkdir -p parent/child
   ```

4. 특정 권한으로 디렉토리 생성:
   ```csh
   mkdir -m 755 mysecurefolder
   ```

5. 생성된 디렉토리 정보 출력:
   ```csh
   mkdir -v newfolder
   ```

## Tips
- 디렉토리를 생성할 때, 항상 현재 작업 디렉토리를 확인하세요.
- `-p` 옵션을 사용하면 중첩된 디렉토리를 쉽게 생성할 수 있습니다.
- 권한 설정이 필요한 경우, `-m` 옵션을 활용하여 보안을 강화하세요.