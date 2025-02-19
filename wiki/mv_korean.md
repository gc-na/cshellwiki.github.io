# [리눅스] C Shell (csh) mv 사용법: 파일 및 디렉토리 이동 및 이름 변경

## Overview
`mv` 명령은 파일이나 디렉토리를 다른 위치로 이동하거나 이름을 변경하는 데 사용됩니다. 이 명령은 파일 시스템 내에서 파일의 위치를 쉽게 조정할 수 있게 해줍니다.

## Usage
기본 구문은 다음과 같습니다:

```
mv [옵션] [인수]
```

## Common Options
- `-i`: 대상 파일이 이미 존재하는 경우, 덮어쓰기를 하기 전에 사용자에게 확인을 요청합니다.
- `-u`: 소스 파일이 대상 파일보다 새롭거나 대상 파일이 존재하지 않을 경우에만 이동합니다.
- `-v`: 이동하는 파일의 이름을 출력합니다.

## Common Examples
- 파일 이름 변경:
  ```bash
  mv oldname.txt newname.txt
  ```

- 파일 이동:
  ```bash
  mv myfile.txt /path/to/destination/
  ```

- 여러 파일을 한 번에 이동:
  ```bash
  mv file1.txt file2.txt /path/to/destination/
  ```

- 파일을 이동하면서 덮어쓰기 전에 확인 요청:
  ```bash
  mv -i myfile.txt /path/to/destination/
  ```

## Tips
- 항상 중요한 파일을 이동하기 전에 백업을 해두는 것이 좋습니다.
- `-v` 옵션을 사용하여 어떤 파일이 이동되는지 확인하면 실수를 줄일 수 있습니다.
- 대량의 파일을 이동할 때는 `-u` 옵션을 사용하여 불필요한 덮어쓰기를 피할 수 있습니다.