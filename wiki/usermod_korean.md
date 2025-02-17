# [리눅스] Bash usermod 사용법: 사용자 계정 수정

## Overview
`usermod` 명령어는 리눅스 시스템에서 사용자 계정의 속성을 수정하는 데 사용됩니다. 이 명령어를 통해 사용자 이름, 그룹, 홈 디렉토리, 로그인 셸 등을 변경할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
usermod [옵션] [사용자 이름]
```

## Common Options
- `-l, --login NEW_LOGIN`: 사용자 이름을 NEW_LOGIN으로 변경합니다.
- `-d, --home NEW_HOME`: 사용자의 홈 디렉토리를 NEW_HOME으로 변경합니다.
- `-m, --move-home`: 홈 디렉토리를 새 위치로 이동합니다.
- `-G, --groups GROUP1[,GROUP2,...]`: 사용자가 속한 그룹을 설정합니다.
- `-s, --shell SHELL`: 사용자의 로그인 셸을 SHELL로 변경합니다.

## Common Examples
1. 사용자 이름 변경:
   ```bash
   usermod -l newusername oldusername
   ```

2. 홈 디렉토리 변경:
   ```bash
   usermod -d /new/home/directory username
   ```

3. 홈 디렉토리 이동:
   ```bash
   usermod -d /new/home/directory -m username
   ```

4. 그룹 추가:
   ```bash
   usermod -aG groupname username
   ```

5. 로그인 셸 변경:
   ```bash
   usermod -s /bin/bash username
   ```

## Tips
- 사용자 계정을 수정하기 전에 항상 백업을 해두는 것이 좋습니다.
- `usermod` 명령어는 루트 권한이 필요하므로 `sudo`를 사용해야 할 수 있습니다.
- 변경 사항이 즉시 반영되지 않을 수 있으므로, 변경 후에는 시스템에 다시 로그인하는 것이 좋습니다.