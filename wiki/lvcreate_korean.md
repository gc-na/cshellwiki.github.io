# [리눅스] Bash lvcreate 사용법: 논리 볼륨 생성

## Overview
`lvcreate` 명령어는 리눅스에서 논리 볼륨을 생성하는 데 사용됩니다. 이 명령어는 LVM(Logical Volume Manager) 환경에서 새로운 논리 볼륨을 만들기 위해 필요합니다.

## Usage
기본 구문은 다음과 같습니다:
```
lvcreate [옵션] [인수]
```

## Common Options
- `-n, --name <name>`: 생성할 논리 볼륨의 이름을 지정합니다.
- `-L, --size <size>`: 생성할 논리 볼륨의 크기를 지정합니다.
- `-l, --extents <extents>`: 논리 볼륨의 크기를 확장 단위로 지정합니다.
- `-C, --mirrors <number>`: 미러링할 논리 볼륨의 수를 지정합니다.

## Common Examples
- **기본 논리 볼륨 생성**
  ```bash
  lvcreate -n my_volume -L 10G my_volume_group
  ```
  위 명령어는 `my_volume_group` 그룹 내에 `my_volume`이라는 이름의 10GB 논리 볼륨을 생성합니다.

- **확장 단위로 논리 볼륨 생성**
  ```bash
  lvcreate -n my_extents_volume -l 100 my_volume_group
  ```
  이 명령어는 `my_volume_group` 내에 100개의 확장 단위로 구성된 `my_extents_volume`을 생성합니다.

- **미러링된 논리 볼륨 생성**
  ```bash
  lvcreate -n my_mirrored_volume -L 20G -m 1 my_volume_group
  ```
  위 명령어는 `my_volume_group` 내에 20GB 크기의 미러링된 논리 볼륨을 생성합니다.

## Tips
- 논리 볼륨을 생성하기 전에 항상 필요한 볼륨 그룹이 존재하는지 확인하세요.
- 볼륨 이름은 명확하고 이해하기 쉽게 지정하는 것이 좋습니다.
- 논리 볼륨을 생성한 후에는 파일 시스템을 생성하고 마운트하는 것을 잊지 마세요.