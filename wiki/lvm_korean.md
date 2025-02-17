# [리눅스] Bash lvm 사용법: 논리 볼륨 관리

## Overview
lvm 명령어는 리눅스에서 논리 볼륨 관리(LVM)를 위한 도구입니다. 이를 통해 사용자는 물리적 볼륨을 그룹화하고, 논리 볼륨을 생성 및 관리할 수 있으며, 저장 공간을 유연하게 조정할 수 있습니다.

## Usage
lvm 명령어의 기본 구문은 다음과 같습니다:

```bash
lvm [options] [arguments]
```

## Common Options
- `create`: 새로운 논리 볼륨을 생성합니다.
- `remove`: 기존 논리 볼륨을 삭제합니다.
- `extend`: 기존 논리 볼륨의 크기를 늘립니다.
- `reduce`: 기존 논리 볼륨의 크기를 줄입니다.
- `lvdisplay`: 논리 볼륨의 정보를 표시합니다.

## Common Examples
- 새로운 논리 볼륨 생성하기:
```bash
lvcreate -n my_volume -L 10G my_volume_group
```

- 논리 볼륨 삭제하기:
```bash
lvremove /dev/my_volume_group/my_volume
```

- 논리 볼륨 크기 늘리기:
```bash
lvextend -L +5G /dev/my_volume_group/my_volume
```

- 논리 볼륨 크기 줄이기:
```bash
lvreduce -L -5G /dev/my_volume_group/my_volume
```

- 논리 볼륨 정보 확인하기:
```bash
lvdisplay /dev/my_volume_group/my_volume
```

## Tips
- 논리 볼륨의 크기를 줄이기 전에 반드시 데이터 백업을 수행하세요.
- 논리 볼륨을 확장할 때는 파일 시스템도 함께 확장해야 합니다.
- LVM을 사용하여 스냅샷을 생성하면 데이터 복구가 용이합니다.