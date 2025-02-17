# [리눅스] Bash vgcreate 사용법: 볼륨 그룹 생성

## Overview
`vgcreate` 명령은 리눅스에서 논리 볼륨 관리(LVM)를 사용하여 새로운 볼륨 그룹을 생성하는 데 사용됩니다. 볼륨 그룹은 여러 물리적 볼륨을 하나의 논리적 저장소로 결합하여 관리할 수 있게 해줍니다.

## Usage
기본 구문은 다음과 같습니다:
```
vgcreate [options] [arguments]
```

## Common Options
- `-s, --stripes <n>`: 볼륨 그룹의 스트라이프 수를 설정합니다.
- `-p, --max-pvs <n>`: 볼륨 그룹에 포함될 수 있는 최대 물리적 볼륨 수를 지정합니다.
- `-f, --force`: 기존 볼륨 그룹을 덮어쓰도록 강제합니다.

## Common Examples
1. 기본 볼륨 그룹 생성:
   ```bash
   vgcreate my_volume_group /dev/sda1 /dev/sda2
   ```
   이 명령은 `/dev/sda1`과 `/dev/sda2`를 포함하는 `my_volume_group`이라는 볼륨 그룹을 생성합니다.

2. 스트라이프 수 설정:
   ```bash
   vgcreate -s 64k my_striped_group /dev/sdb1 /dev/sdb2
   ```
   이 명령은 64KB 스트라이프를 사용하는 `my_striped_group`이라는 볼륨 그룹을 생성합니다.

3. 최대 물리적 볼륨 수 설정:
   ```bash
   vgcreate -p 10 my_limited_group /dev/sdc1
   ```
   이 명령은 최대 10개의 물리적 볼륨을 포함할 수 있는 `my_limited_group`을 생성합니다.

## Tips
- 볼륨 그룹을 생성하기 전에 물리적 볼륨이 준비되어 있는지 확인하세요.
- `vgdisplay` 명령을 사용하여 생성된 볼륨 그룹의 정보를 확인할 수 있습니다.
- 볼륨 그룹을 생성한 후에는 `lvcreate` 명령을 사용하여 논리 볼륨을 생성할 수 있습니다.