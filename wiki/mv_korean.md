# [리눅스] Bash mv 사용법: 파일 및 디렉토리 이동 및 이름 변경

## Overview
`mv` 명령어는 파일이나 디렉토리를 다른 위치로 이동하거나 이름을 변경하는 데 사용됩니다. 이 명령어는 간단하면서도 매우 유용하여 파일 관리에 자주 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
mv [옵션] [대상] [목적지]
```

## Common Options
- `-i`: 목적지에 같은 이름의 파일이 있을 경우, 덮어쓰기를 하기 전에 확인합니다.
- `-u`: 목적지 파일이 없거나 소스 파일이 더 최신일 경우에만 이동합니다.
- `-v`: 이동하는 파일의 이름을 출력합니다.
- `-n`: 같은 이름의 파일이 있을 경우 덮어쓰지 않습니다.

## Common Examples
1. 파일 이동하기:
   ```bash
   mv file.txt /home/user/documents/
   ```
   `file.txt`를 `/home/user/documents/` 디렉토리로 이동합니다.

2. 파일 이름 변경하기:
   ```bash
   mv oldname.txt newname.txt
   ```
   `oldname.txt`의 이름을 `newname.txt`로 변경합니다.

3. 여러 파일을 한 번에 이동하기:
   ```bash
   mv file1.txt file2.txt /home/user/documents/
   ```
   `file1.txt`와 `file2.txt`를 `/home/user/documents/` 디렉토리로 이동합니다.

4. 덮어쓰기 확인 후 이동하기:
   ```bash
   mv -i file.txt /home/user/documents/
   ```
   같은 이름의 파일이 있을 경우, 덮어쓰기를 하기 전에 확인합니다.

## Tips
- 파일을 이동할 때, 항상 목적지 경로가 올바른지 확인하세요.
- 중요한 파일을 이동할 때는 `-i` 옵션을 사용하는 것이 좋습니다.
- 여러 파일을 동시에 이동할 때는 공백을 주의하여 사용하세요.