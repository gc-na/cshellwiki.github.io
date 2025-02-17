# [리눅스] Bash vgextend 사용법: 논리 볼륨 그룹에 물리 볼륨 추가

## Overview
`vgextend` 명령은 리눅스에서 논리 볼륨 그룹에 새로운 물리 볼륨을 추가하는 데 사용됩니다. 이 명령을 통해 볼륨 그룹의 크기를 확장할 수 있으며, 추가된 물리 볼륨의 공간을 활용하여 더 많은 논리 볼륨을 생성하거나 기존 논리 볼륨의 크기를 늘릴 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
vgextend [옵션] [볼륨 그룹 이름] [물리 볼륨 이름]
```

## Common Options
- `-f`: 강제로 물리 볼륨을 추가합니다.
- `-n`: 추가할 물리 볼륨의 이름을 지정합니다.
- `--test`: 실제로 변경하지 않고 실행할 명령을 테스트합니다.

## Common Examples
1. **물리 볼륨 추가하기**
   ```bash
   vgextend my_volume_group /dev/sdb1
   ```
   위 명령은 `my_volume_group`이라는 논리 볼륨 그룹에 `/dev/sdb1` 물리 볼륨을 추가합니다.

2. **여러 물리 볼륨 추가하기**
   ```bash
   vgextend my_volume_group /dev/sdb1 /dev/sdc1
   ```
   이 명령은 `my_volume_group`에 `/dev/sdb1`과 `/dev/sdc1` 두 개의 물리 볼륨을 추가합니다.

3. **강제로 물리 볼륨 추가하기**
   ```bash
   vgextend -f my_volume_group /dev/sdb1
   ```
   `-f` 옵션을 사용하여 강제로 물리 볼륨을 추가합니다.

4. **테스트 모드로 실행하기**
   ```bash
   vgextend --test my_volume_group /dev/sdb1
   ```
   `--test` 옵션을 사용하여 실제로 변경하지 않고 어떤 일이 발생할지를 확인합니다.

## Tips
- 물리 볼륨을 추가하기 전에 항상 현재 볼륨 그룹의 상태를 확인하세요.
- `vgdisplay` 명령을 사용하여 볼륨 그룹의 정보를 확인할 수 있습니다.
- 추가한 물리 볼륨의 공간을 활용하기 위해서는 논리 볼륨을 확장하는 `lvextend` 명령을 사용해야 합니다.