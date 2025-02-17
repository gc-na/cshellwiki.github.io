# [리눅스] Bash alias 사용법: 명령어 단축

## Overview
`alias` 명령어는 사용자가 자주 사용하는 명령어를 짧고 간단한 이름으로 정의할 수 있게 해줍니다. 이를 통해 긴 명령어를 입력하는 번거로움을 줄이고, 작업 효율성을 높일 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
alias [options] [name]='[command]'
```

## Common Options
- `-p`: 현재 정의된 모든 alias 목록을 출력합니다.
- `-d`: 지정한 alias를 삭제합니다.

## Common Examples
다음은 `alias` 명령어의 몇 가지 실용적인 예시입니다.

1. **간단한 alias 생성**
   ```bash
   alias ll='ls -la'
   ```
   이 명령어는 `ll`을 입력하면 `ls -la` 명령어가 실행되도록 합니다.

2. **복잡한 명령어 alias 생성**
   ```bash
   alias gs='git status'
   ```
   `gs`를 입력하면 `git status`가 실행됩니다.

3. **alias 목록 보기**
   ```bash
   alias -p
   ```
   현재 정의된 모든 alias를 확인할 수 있습니다.

4. **alias 삭제**
   ```bash
   unalias ll
   ```
   `ll` alias를 삭제합니다.

## Tips
- 자주 사용하는 명령어를 alias로 정의하면 작업 속도가 빨라집니다.
- `.bashrc` 파일에 alias를 추가하면 터미널을 열 때마다 자동으로 적용됩니다.
- alias 이름은 짧고 기억하기 쉬운 것으로 설정하는 것이 좋습니다.