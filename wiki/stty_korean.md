# [리눅스] C Shell (csh) stty 사용법: 터미널 속성 설정

## Overview
`stty` 명령어는 터미널의 속성을 설정하고 조정하는 데 사용됩니다. 이 명령어를 통해 입력 및 출력 설정을 변경하고, 터미널의 동작 방식을 제어할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```csh
stty [options] [arguments]
```

## Common Options
- `-a`: 현재 터미널의 모든 설정을 표시합니다.
- `-g`: 현재 설정을 저장할 수 있는 형식으로 출력합니다.
- `-F <file>`: 지정된 파일에 대한 터미널 설정을 변경합니다.
- `intr <char>`: 인터럽트 문자를 설정합니다.
- `erase <char>`: 지우기 문자를 설정합니다.

## Common Examples
- 현재 터미널 설정 보기:
  ```csh
  stty -a
  ```

- 인터럽트 문자 설정하기 (예: Ctrl+C):
  ```csh
  stty intr ^C
  ```

- 지우기 문자 설정하기 (예: Backspace):
  ```csh
  stty erase ^H
  ```

- 터미널 설정을 파일로 저장하기:
  ```csh
  stty -g > settings.txt
  ```

- 파일에서 터미널 설정 복원하기:
  ```csh
  stty < settings.txt
  ```

## Tips
- `stty -a`를 사용하여 현재 설정을 확인한 후, 필요한 옵션을 조정하는 것이 좋습니다.
- 설정을 변경하기 전에 현재 설정을 백업하는 것이 유용합니다.
- 특정 프로그램이 요구하는 터미널 설정이 있을 수 있으므로, 프로그램 문서를 참조하는 것이 좋습니다.