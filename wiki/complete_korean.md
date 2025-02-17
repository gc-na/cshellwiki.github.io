# [리눅스] Bash complete 사용법: 명령어 자동 완성

## Overview
`complete` 명령어는 Bash 셸에서 명령어의 자동 완성을 설정하는 데 사용됩니다. 사용자가 특정 명령어를 입력할 때, 이 명령어는 해당 명령어에 대한 자동 완성 옵션을 정의하여 입력을 더 빠르고 효율적으로 만들어 줍니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
complete [options] [arguments]
```

## Common Options
- `-A`: 자동 완성 유형을 지정합니다. 예를 들어, `-A command`는 명령어 자동 완성을 설정합니다.
- `-o`: 특정 옵션을 추가합니다. 예를 들어, `-o nospace`는 자동 완성 후 공백을 추가하지 않도록 설정합니다.
- `-F`: 사용자 정의 함수로 자동 완성을 설정합니다.

## Common Examples

1. **기본 명령어 자동 완성 설정**
   ```bash
   complete -A command mycmd
   ```
   위 명령어는 `mycmd`에 대해 기본 명령어 자동 완성을 설정합니다.

2. **사용자 정의 함수로 자동 완성 설정**
   ```bash
   _my_custom_function() {
       COMPREPLY=( $(compgen -W "option1 option2 option3" -- "${COMP_WORDS[COMP_CWORD]}") )
   }
   complete -F _my_custom_function mycmd
   ```
   이 예제는 `mycmd`에 대해 사용자 정의 함수 `_my_custom_function`을 사용하여 자동 완성을 설정합니다.

3. **옵션 없이 자동 완성 설정**
   ```bash
   complete mycmd
   ```
   이 명령어는 `mycmd`에 대해 기본 자동 완성을 설정합니다.

## Tips
- 자동 완성을 설정할 때, 명령어의 사용 패턴을 고려하여 적절한 옵션을 선택하세요.
- 사용자 정의 함수를 사용할 경우, 함수 내에서 `COMPREPLY` 배열을 적절히 설정하여 원하는 자동 완성 항목을 제공하세요.
- `.bashrc` 파일에 자동 완성 설정을 추가하면, 셸을 시작할 때마다 자동으로 적용됩니다.