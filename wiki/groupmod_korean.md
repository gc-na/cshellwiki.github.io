# [리눅스] Bash groupmod 사용법: 그룹 수정

## Overview
`groupmod` 명령어는 기존 그룹의 속성을 수정하는 데 사용됩니다. 이 명령어를 통해 그룹 이름이나 그룹 ID(GID)를 변경할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
groupmod [options] [arguments]
```

## Common Options
- `-n, --new-name`: 그룹의 새 이름을 지정합니다.
- `-g, --gid`: 그룹의 새 GID를 설정합니다.
- `-o, --non-unique`: GID가 고유하지 않은 경우에도 사용하도록 허용합니다.

## Common Examples
1. 그룹 이름 변경:
   ```bash
   groupmod -n newgroup oldgroup
   ```
   이 명령어는 `oldgroup`이라는 그룹의 이름을 `newgroup`으로 변경합니다.

2. 그룹 ID 변경:
   ```bash
   groupmod -g 1001 mygroup
   ```
   이 명령어는 `mygroup`의 GID를 1001로 변경합니다.

3. 비고유 GID 설정:
   ```bash
   groupmod -o -g 1001 anothergroup
   ```
   이 명령어는 `anothergroup`의 GID를 1001로 설정하되, 다른 그룹과 중복될 수 있도록 허용합니다.

## Tips
- 그룹 이름이나 GID를 변경할 때는 해당 그룹에 속한 사용자 계정의 설정도 함께 고려해야 합니다.
- 변경 후에는 관련된 서비스나 애플리케이션이 영향을 받을 수 있으므로, 변경 사항을 신중하게 검토하십시오.
- `groupmod` 명령어를 사용하기 전에 `groupadd`와 `groupdel` 명령어를 통해 그룹을 추가하거나 삭제하는 방법도 익혀두면 좋습니다.